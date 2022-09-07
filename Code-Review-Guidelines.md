# CODE REVIEW - Journey Horizon Guideline

This guidelines would have 4 sections, one for the reviewer and one for the one that got reviewed.

## Table of Contents

1. [Why should we have "code review"?](#1-why-should-we-have-code-review)
  - [1.1) Sharing knowledge](#11-sharing-knowledge)
  - [1.2) Spreading ownership](#12-spreading-ownership)
  - [1.3) Unifying development practices](#13-unifying-development-practices)
  - [1.4) Quanlity control](#14-quanlity-control)
2. [Our Code review process](#2-our-code-review-process)
  - [2.1) Draft state](#21-draft-state)
  - [2.2) Ready to Review](#22-ready-to-review)
  - [2.3) Changes requested](#23-changes-requested)
  - [2.4) Approved](#24-approved)
3. [Code Design for Review](#3-code-design-for-review-prepare-for-a-final-pr)
  - [3.1) Intentional bad designs or dirty work](#31-intentional-bad-designs-or-dirty-work)
  - [3.2) The comments](#32-the-comments)
  - [3.3) Explaining Complicated works](#33-explaining-complicated-works)
  - [3.4) If you are copying an existing file then modified it](#34-if-you-are-copying-an-existing-file-then-modified-it)
  - [3.5) If your feature involves multiple branches](#35-if-your-feature-involves-multiple-branches)
  - [3.6) Avoid auto-formatting all files](#36-avoid-auto-formatting-all-files)
  - [3.7) Resolve merge conflict](#37-resolve-merge-conflict)
  - [3.8) When to ask for a review](#38-when-to-ask-for-a-review)
4. [Code Review](#4-code-review)
  - [4.3) Focus on the right things](#41-focus-on-the-right-things)
  - [4.2) Logic Review](#42-logic-review)
    - [Preparation](#preparation)
      - [General](#general)
      - [Specialized logic](#specialized-logic)
    - [Question to ask when reviewing](#question-to-ask-when-reviewing)
    - [Reverting to the Reviewee](#reverting-to-the-reviewee)
    - [Priorities](#priorities)
  - [4.3) UI/UX Review](#43-uiux-review)
  - [4.4) Notice for reviewer](#44-notice-for-reviewer)
5. [Optimize Code review](#5-optimize-code-review)
  - [5.1) Code review help us to have a "better source code" not the "best source code"](#51-code-review-help-us-to-have-a-better-source-code-not-the-best-source-code)
  - [5.2) Speed to review](#52-speed-to-review)
  - [5.3) Deal with stuck](#53-deal-with-stuck)
  - [5.4) Foster a positive feedback culture](#54-foster-a-positive-feedback-culture)
  - [5.5) Communicate explicitly](#55-communicate-explicitly)
  - [5.6) Review your own code](#56-review-your-own-code)
  - [5.7) Document as much as possible in code](#57-document-as-much-as-possible-in-code)
  - [5.8) Write clear PR descriptions](#58-write-clear-pr-descriptions)
  - [5.9) Keep discussions public](#59-keep-discussions-public)
  - [5.10) Resolving People conflict when doing code review](#510-resolving-people-conflict-when-doing-code-review)


----------------------------------


# 1) Why should we have "code review"?

Remember that, code review will not help us to have "best code", it help us to have "better code", so don't try to spend a lot of time to optimize to have a perfect code.

## 1.1) Sharing knowledge

- I know that we do not have much time for code review to scan and understand full of others' code, but some amount of information will always be transferred between members. The knowledge can be general tips about the framework, library or programming language, software design principles or invaluable domain-specific information bits.
- It’s always fine to leave comments that help a developer learn something new. Sharing knowledge is part of improving the code health of a system over time. (Just keep in mind that if your comment is purely educational, but not critical to meeting the standards described in this document, prefix it with “Suggestion: “ or otherwise indicate that it’s not mandatory for the author to resolve it in the PR).

## 1.2) Spreading ownership

- Code reviews have a positive impact on mutual code ownership. It's easy to end up in a situation where one developer always deals with a certain part of the codebase because they're most familiar with it. It might be a short-term win but is often a long-term loss. When ownership is shared, teams become more motivated and autonomous.

## 1.3) Unifying development practices

- Every developer has their own tendencies and ways to implement software (functions, features, UI, UX, apis, server). Code reviews help to narrow the gap between individual development styles and make the codebase more unified. Unification happens through high-level discussions about architecture and software design and via logic and ui styling checks, such as coding convention enforcement.

## 1.4) Quanlity control

- Code reviews can help with catching defects, but even more importantly, they surface software design issues while they are still relatively easy to change. Instead of spending too much time for Tester and SE to find and reproduce bugs then try to fix a very small misktake in coding, we may resolve it very quickly in code review process. Less small bugs, shorter time to release features to clients.


----------------------------------


# 2) Our Code review process

- To reduce confusing when do a code review process and unify our practice, here is a process for code review:
  
## 2.1) Draft state

- You can open a PR in a draft state to show progress or request early feedback.
- Which Draft state please add a status into PR name, such as "**[Draft]Create new carousel on homepage hero section**"
- When you ready to have final PR, please remove Draft status by removing "**[Draft]**" in PR name, such as "**Create new carousel on homepage hero section**".

## 2.2) Ready to Review

- You can also skip the Draft state and open a normal PR directly.
- The review is done by another team member.
- Remember to resolve conflict before assign reviewer [How to resolve confict in right way](#here)
- Remember to assign reviewer
- Remember to note all neccessary things into PR description: 
  - Environment variables.
  - Important notes, warnings.
  - Guideline how to integrate and deploy
- Reviewers will join and send reviews and feedbacks.

- **[Will implement in future][Leave it for now]** *Usually, there's no need to request a review (Assign reviewer); Our bots automatically notifies the team.*

## 2.3) Changes requested

- Fix the requested changes, or discuss whether a fix is needed.
- Reviewers re-check changes.
- Preferably, create new commits after the review.

## 2.4) Approved

- Remember to read notes on PR description: 
  - Environment variables.
  - Important notes, warnings.
  - Guideline how to integrate and deploy
- The author is responsible for merging their own PR on Test site.
- How about production? Depend on the team?.


----------------------------------


# 3) Code Design for Review (Prepare for a Final PR)

Your code should ensure these things before a review was asked:

## 3.1) Intentional bad designs or dirty work 

Any bad designs or dirty works should be commented properly on where it was coded, explaining the full intention.

## 3.2) The comments

The comments for dirty work, or bad designs should includes these 3 things:
  - Why - why did you make it dirty
  - Technical Debt - what could go wrong
  - Solution (optional) - how can we fix this in the future?

## 3.3) Explaining Complicated works

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

## 3.4) If you are copying an existing file then modified it

You should state clearly in the PR by leaving comment on what was changed. It would save a lot of time for the reader to understand what you changed instead of going through an entire files.

## 3.5) If your feature involves multiple branches

You should note it to the reviewer what branches your feature was based on. 

## 3.6) Avoid auto-formatting all files

You should only format the files that you touched, don't do auto-formatting all files because it would includes files that was not in your features. This would create code noise for the reviewer.

You can format a file if you find it format is too irritating and can't be read but make sure that you know what you are doing.

## 3.7) Resolve merge conflict

If we have a confict when merge code, please checkout new branch from destination branch, then merge our feature branch into new branch and resolve conflict in that new branch, then create PR from new branch to destination branch.

## 3.8) When to ask for a review

At the moment of this writing, each team is having a rules of it owns, we would discuss this further but as of now, follow your PM's instruction for when to ask for a review since some team would do it in a pre-defined time while some allow the freedom of asking.


----------------------------------


# 4) Code Review

Review is communication process, there are plenty of things you can do for a review, this should only be a basic list of what you can do, not an exhaust list so you can always add more of your flavour to the review.

## 4.1) Focus on the right things

Remember that, code review will not help us to have "best code", it help us to have "better code", so don't try to spend a lot of time to optimize to have a perfect code.

Before going to review, we need to know which we should focus on in code reviews. Here's what we recommend focusing on:
- **Functionality**: Does the code behave as the PR author likely intended? Does the code behave as users would expect?
- **Software design**: Is the code well-designed and fitted to the surrounding architecture?
- **Complexity**: Would another developer be able to easily understand and use the code?
- **Naming**: Are names for variables, functions, etc. descriptive?
- **Comments**: Are the comments clear and useful?
- **Documentation**: Did the author also update relevant documentation?

- **[Will implement in future][Leave it for now]** *Tests: Does the PR have correct and well-designed automated tests?*

In the future we will implement some automatically checking bot to save your time, then developers shouldn't spend their time reviewing things that can be automatically checked.

## 4.2) Logic Review

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

## 4.3) UI/UX Review

Beside logic, UI/UX is an important thing for a project, but most of developers forget or feel too hard and take times to do it a review for HTML/CSS and Layout stuff. Therefore here is some note for you to ensure a better UI/UX code in a faster and easy way.

## 4.4) Notice for Reviewer

- Just keep in mind that if your comment is purely educational, but not critical to meeting the standards described in this document, prefix it with “Suggestion: “ or otherwise indicate that it’s not mandatory for the author to resolve it in the PR.


----------------------------------


# 5) Optimize Code review & FAQ

In reality, when do a review, we face a lot of problems that we can get stuck in our flow and process. We will discuss how to deal with these problems here.

## 5.1) Code review help us to have a "better source code" not the "best source code"

- Remember that, code review will not help us to have "best code", it help us to have "better code", so don't try to spend a lot of time to optimize to have a perfect code. Reviewers should not require the author to polish every tiny piece of a PR before granting approval. Rather, the reviewer should balance out the need to make forward progress compared to the importance of the changes they are suggesting. Instead of seeking perfection, what a reviewer should seek is continuous improvement. A PR that, as a whole, improves the maintainability, readability, and understandability of the system shouldn’t be delayed for days or weeks because it isn’t “perfect.”

- Reviewers should always feel free to leave comments expressing that something could be better, but if it’s not very important, prefix it with something like “Suggestion: “ to let the author know that it’s just a point of polish that they could choose to ignore.

## 5.2) Speed to review

- Speedy reviews increase team performance in multiple ways: iteration becomes faster, developers don't need to do time-costly context switches as often, etc. Make sure the team understands the implications of fast reviews and agrees on a suitable maximum time for responding to a PR. The key is to minimize the response lag between the author and the reviewer, even if the whole review process takes long.

- If you are not in the middle of a focused task, you should do a code review shortly after it comes in.

- One business day is the maximum time it should take to respond to a code review request (i.e., first thing the next morning).

- A typical PR should get multiple rounds of review (if needed) within a single day.

- There is one time where the consideration of personal velocity trumps team velocity. If you are in the middle of a focused task, such as writing code, don’t interrupt yourself to do a code review. Research has shown that it can take a long time for a developer to get back into a smooth flow of development after being interrupted. So interrupting yourself while coding is actually more expensive to the team than making another developer wait a bit for a code review. Instead, wait for a break point in your work before you respond to a request for review. This could be when your current coding task is completed, after lunch, returning from a meeting, coming back from the breakroom, etc.

- Review speed is definitely not solely the reviewer's responsibility—the author has an important role too. The easier it is to pick a pull request and review it, the faster the work flows.

## 5.3) Deal with stuck

- Sometimes reviews can stall for various reasons. During those times, you should have a bias for action. One can approve a PR even if there's some input left for the author to consider.

- If a tech decision lingers and work becomes blocked, deciding something relatively quickly is better than slowly concluding to an "ideal" decision. Reserve enough time for technical decisions, but move on before you reach analysis paralysis. Developers should be inclined to merge code instead of primarily focusing on poking holes in the implementation.

## 5.4) Foster a positive feedback culture

Effective communication, in general, is really hard. Giving feedback about a colleague's work is one of the most challenging forms of communication. Acknowledge this in code reviews.

Here's a list of suggestions to improve discussions in code reviews:

- Give feedback about the code, not about the PR author.
- Select correct topic or problem you want to discuss, if you think it is small and you don't have skill to support, just leave it for others.
- Accept that there are multiple correct solutions to a problem.
- You're in the same boat (same company).
- PR authors are humans with feelings (except dependabot 🤖).
- Provide reasons, not feelings, to support your position.
- Use the "Yes, and..." technique to keep an innovative atmosphere. It can be an ungracious pattern to dismiss fresh and fragile ideas in a draft PR stage.
- Keep the feedback balanced with positive comments. It's always delightful to receive praise from the reviewer.

If the pull request discussion becomes heated, schedule a call to discuss the topic. It usually helps to relieve the tension.

## 5.5) Communicate explicitly

As we said above in [3](#3-code-design-for-review-prepare-for-a-final-pr) and [4](#4-code-review), Please try to explain and communicate explicity to avoid misunderstanding.

- When reviewing a piece of code, be explicit about the action you request from the author. Let's say a reviewer has commented, "This could be done in Postgres in favor of application code" on a line of code. Are they requesting a change, suggesting to refactor it later, or just making the author aware of other solutions? It's often hard to judge. GitHub provides tools to be more explicit: for example, "Request changes" in a review.

- Tip for the PR author: dismissing a review resets the pull request state to indicate that the reviewer can review again. It's up to you, the PR author, to decide if it feels important enough to use the feature, but especially in remote teams, it might help to make the process even more explicit.

## 5.6) Review your own code

- Before submitting a PR for a review, go through the changes yourself. This helps to catch accidentally included changes, typos, and other simple mistakes that potentially waste the reviewer's time.

## 5.7) Document as much as possible in code

- When receiving a comment or suggestion, aim for documenting the discussion in code. If the reviewer is not sure what the validateUsers function does, elaborate on the functionality ideally by renaming the function or writing a comment in the code. This way, the next developer that reads the code will understand the functionality without reading the PR discussions.

- In some cases, the author can copy-paste their PR discussion response as is to comment in the code.

## 5.8) Write clear PR descriptions

- The reviewer forms a mental picture of a pull request from multiple information sources: feature planning, description in the issue tracker, PR description, commit messages, chat history, etc. The more coherent the picture is, the faster and higher quality the review is. Decide on the team’s preferred channels to communicate certain information.

- We use PR descriptions to fill the technical information like ENV Variable, guideline how to integrate and deploy, special notes and warnings: these information will help us to show what setup is needed to test the PR, surprising implementation details, and anything that makes the reviewer's job smoother. Beside PR description, there are also other ways to add information: code comments, commit messages, commenting on individual lines in a PR as the author, etc.

- Demo in any visual form is a nice touch. The format can be a screenshot, a screen capture, terminal output pasted in a code block, or anything that captures the change well. GitHub supports both videos and GIFs in the PR descriptions.

- **[Will consider more in the future how to do it in easy and fast way]** *In addition to a static demo video, it's a great practice to build preview versions of your application per PR branch. The ability to interactively test the application preview without setting up anything in a local development environment saves time and increases the likelihood of someone manually testing a pull request.*

## 5.9) Keep discussions public

- It's convenient to have a quick chat about a pull request in the office, but be mindful of colleagues working remotely. It's polite to add a summary of face-to-face discussion as a PR comment.

- Pull request discussions are searchable and easily accessible by all developers. They act as a history log of discussion which might be incredibly valuable when debugging a production incident later on.


## 5.10) Resolving People conflict when doing code review

- In any conflict on a code review, the first step should always be for the developer and reviewer to try to come to consensus, based on the contents of this document and the other convention documents.

- When coming to consensus becomes especially difficult, it can help to have a face-to-face meeting or a video conference between the reviewer and the author, instead of just trying to resolve the conflict through code review comments. (If you do this, though, make sure to record the results of the discussion as a comment on the PR, for future readers.)

- If that doesn’t resolve the situation, the most common way to resolve it would be to escalate. Often the escalation path is to a broader team discussion, having a Technical Coordinator weigh in, asking for a decision from a maintainer of the code, or asking an Manager to help out. Don’t let a PR sit around because the author and the reviewer can’t come to an agreement.