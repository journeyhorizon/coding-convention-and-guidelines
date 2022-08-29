This guidelines would have 2 sections, one for the reviewer and one for the one that got reviewed.
- [Code Design for Review](#code-design-for-review)
  - [1) Intentional bad designs or dirty work](#1-intentional-bad-designs-or-dirty-work)
  - [2) The comments](#2-the-comments)
  - [3) Explaining Complicated works](#3-explaining-complicated-works)
  - [4) If you are copying an existing file then modified it](#4-if-you-are-copying-an-existing-file-then-modified-it)
  - [5) If your feature involves multiple branches](#5-if-your-feature-involves-multiple-branches)
  - [6) Avoid auto-formatting all files](#6-avoid-auto-formatting-all-files)
  - [7) When to ask for a review](#7-when-to-ask-for-a-review)
- [Code Review](#code-review)
  - [1) Logic Review](#1-logic-review)
    - [Preparation](#preparation)
      - [General](#general)
      - [Specialized logic](#specialized-logic)
    - [Question to ask when reviewing](#question-to-ask-when-reviewing)
    - [Reverting to the Reviewee](#reverting-to-the-reviewee)
    - [Priorities](#priorities)

# Code Design for Review

Your code should ensure these things before a review was asked:
## 1) Intentional bad designs or dirty work 

Any bad designs or dirty works should be commented properly on where it was coded, explaining the full intention.
## 2) The comments

The comments for dirty work, or bad designs should includes these 3 things:
  - Why - why did you make it dirty
  - Technical Debt - what could go wrong
  - Solution (optional) - how can we fix this in the future?

## 3) Explaining Complicated works

The complicated parts should have comment explaining what it does, your code should always be self-explained. But we do not live in a perfect world, there bound to be things we have to do it with high complexity. In such cases, always remember to write out your code flow for other to understand.

Ex:

Look at the current code, what is the problem with it?

```js
const createTransferwireAccount = async (req, res) => {
  try {
    return composePromises(
      fetchUserAndCreateRecipientAccount,
      updateUserProfile,
      finaliseResponse(res)
    )(req)

  } catch (e) {
    handleError(res, e);
  }
}
```

It looks like the code is fetching user data, create and an account from Transferwise. But here is the problem - The code does not verify the client's request so there is potential for hacker to inject data that was not validated properly. If you as the write who know about this, but because of limited time, you decided to skip the checkout, you should leave out comment here like this:

```js
/**
 * TODO:JH implement webhook to listen to user's onboarding success event
 * TODO: Figure out potential security risk here further
 * We are not verifying any data from the client, we just passed them onto Transferwise at the moment
 */

const createTransferwireAccount = async (req, res) => {
  try {
    return composePromises(
      fetchUserAndCreateRecipientAccount,
      updateUserProfile,
      finaliseResponse(res)
    )(req)

  } catch (e) {
    handleError(res, e);
  }
}
```

## 4) If you are copying an existing file then modified it

You should state clearly in the PR by leaving comment on what was changed. It would save a lot of time for the reader to understand what you changed instead of going through an entire files.

## 5) If your feature involves multiple branches

You should note it to the reviewer what branches your feature was based on. 

## 6) Avoid auto-formatting all files

You should only format the files that you touched, don't do auto-formatting all files because it would includes files that was not in your features. This would create code noise for the reviewer.

You can format a file if you find it format is too irritating and can't be read but make sure that you know what you are doing.

## 7) When to ask for a review

At the moment of this writing, each team is having a rules of it owns, we would discuss this further but as of now, follow your PM's instruction for when to ask for a review since some team would do it in a pre-defined time while some allow the freedom of asking.

# Code Review

Review is communication process, there are plenty of things you can do for a review, this should only be a basic list of what you can do, not an exhaust list so you can always add more of your flavour to the review.

## 1) Logic Review

### Preparation

#### General

Always make sure you understand the following thing before diving onto a logical code part:
- The expected outcome - you should know before hand what the outcome should look like.
- The scenario that the code is trying to solve - the logical part might be a part of a bigger code routine. You should have a rough ideas of what the problem the code is trying to solve that way you could deduct if the current logical part is needed or can be done another way.

#### Specialized logic

You would mostly likely have to reviewed features that has lots of things you understand, at that point, you should always `communicate` to the reviewee and the PM about that fact. There are 2 ways to go from here:
1) You need to do your own reading on the subject
2) Ask for another reviewer who has the knowledge to step in

On what options to choose, it would depend on your workload, if you have too much work, revert to your PM for help in getting another reviewer to help.

### Question to ask when reviewing

When reviewing always ask yourself these questions:
1) Why is it code like this?
2) Are there any other solution?
3) What would you do if you are the person to do this?
4) Is the current code over-deal the current scenario? 
5) Is the code understandable?

### Reverting to the Reviewee

Always remember to `communicate`, if you find something that can be done another way, can be shorter, hard to understand. `You should always explain` to the reviewee about their code, always be nice and prevent form giving too much orders.

In general a review comment should have these things:
- Why it is bad
- What we can do to make it better
- Examples (optional)

Ex:

Considering this code

```js
module.exports = (req, res) => {
  const { isSpeculative, orderData, bodyParams, queryParams } = req.body;

  const listingId = bodyParams && bodyParams.params ? bodyParams.params.listingId : null;

  const sdk = getSdk(req, res);
  let lineItems = null;

  sdk.listings
    .show({ id: listingId })
    .then(listingResponse => {
      const listing = listingResponse.data.data;
      lineItems = transactionLineItems(listing, { ...orderData, ...bodyParams.params });

      return getTrustedSdk(req);
    })
    .then(trustedSdk => {
      const { params } = bodyParams;

      // Add lineItems to the body params
      const body = {
        ...bodyParams,
        params: {
          ...params,
          lineItems,
        },
      };

      if (isSpeculative) {
        return trustedSdk.transactions.initiateSpeculative(body, queryParams);
      }
      return trustedSdk.transactions.initiate(body, queryParams);
    })
    .then(apiResponse => {
      const { status, statusText, data } = apiResponse;
      res
        .status(status)
        .set('Content-Type', 'application/transit+json')
        .send(
          serialize({
            status,
            statusText,
            data,
          })
        )
        .end();
    })
    .catch(e => {
      handleError(res, e);
    });
};
```

This modules has too many things in its logic, it would violate our backend convention. If you have a better way of doing this, you should always suggest and explain to the reviewee.

You should not write current review like this:
```
fnc too long
```

You can write it like this

```
The function is too long, we can separate each then into a func.
```

Or even better

```
The function is too long, we can separate each then into a func. The finalise response part can be re-used let's make sure to generalize that function as well.
```

### Priorities

The reply that you received from the example review above could look like this

```
Copy from Flex default
```

At this moment you would have choose choice:
1) Still asking to the refactor.
2) Leave it as it is.

Do 1) if there are not much work in the pipelines
Do 2) if the current reviewee is overflowing with works.

In conclusion, always based your priorities based on the actual workload, if in doubt, consult the PMs to make decision.



