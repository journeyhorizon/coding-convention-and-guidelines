- [API Endpoints](#api-endpoints)
  - [Method usage](#method-usage)
  - [Naming](#naming)
  - [Handling errors](#handling-errors)
  - [Handling response](#handling-response)
    - [For getting single entity return](#for-getting-single-entity-return)
    - [For getting array of an entity return:](#for-getting-array-of-an-entity-return)
    - [For entity creation and updating return:](#for-entity-creation-and-updating-return)
    - [For query entities data return](#for-query-entities-data-return)
    - [For returning multiple additional entities for an entity return](#for-returning-multiple-additional-entities-for-an-entity-return)
- [Code Modules](#code-modules)
  - [Priorities](#priorities)
  - [Modules](#modules)
    - [Naming](#naming-1)
    - [Input](#input)
    - [Output](#output)
  - [Composing](#composing)
  - [Comments](#comments)
  - [Environments](#environments)
- [Security](#security)
  - [Authentication](#authentication)
  - [Data](#data)
  - [Do and Do not (will be regularly updated)](#do-and-do-not-will-be-regularly-updated)

# API Endpoints

## Method usage

Use correspond request method for the desired actions, don't just label everything as `POST`.

`GET`: For retrieving resources. Any additional configuration should be includes using query.

`POST`: Only use for creation of resources. 
Ex: If you are creating a new user, you are using `POST `. If you are updating a user, don't use `POST`, use something else.

`PUT` (`PATCH`): Only use for update of existing resources. 
Ex: Updating a user, updating a listing, updating some entity,...etc should use `PUT` (`PATCH`) API endpoints. 

There are some big difference between `PUT` and `PATCH`. `PUT` would usually for replacing entire resources, `PATCH` would be for replacing partially. 
Ex:
Updating a user metadata would be using `PATCH` since it only change a part of the data
Replacing entire user data while keep its id would be using a `PUT`. 

`DELETE`: For deleting resources. Under most circumstances, this endpoint should be accompanied with authentication since this is a destructive actions, it would make no sense to allow anyone to delete a resource unless it was deliberately so.


## Naming

Always separate your endpoint into chunk of resources and make use of the request method to describe what you want, most of the trailing endpoint should only have 1 word, if it's more than 2, it is usually a good sign to split the endpoint into smaller chunk.

Ex:

✅:

creating a new user endpoint should be:
`/api/user` with `POST` method

updating a new user endpoint should be:
`/api/user` with `PUT` or `PATCH` method

deleting a new user endpoint should be:
`/api/user` with `DELETE` method

❌:

creating a new user endpoint should not be:
`/api/createUser`

updating a new user endpoint should not be:
`/api/updateUser`

## Handling errors

Returned error response for an server should always follow this structure, no matter what format you use.

```ts
interface Error {
  name: string; //normal words separte by a *-*
  data?: any;
} 
```

✅:

```js
return {
  name: 'current-user-is-not-admin',
  data: {
    message: 'Current user is only a normal user, only admin can access this'
  }
}
```

❌:

```js
//Missing name
return {
  data: {
    message: 'Current user is only a normal user, only admin can access this'
  }
}

//Using normal characters for error name
return {
  name: 'forbidden',
  data: {
    message: 'Current user is only a normal user, only admin can access this'
  }
}
```

## Handling response

Returned response must always follow this structure no matter what:

### For getting single entity return
```ts
interface Response {
  data: Object;
} 
```

Ex: 

✅:

```ts
return {
  data: {
    id: 1,
    name: 'foo',
    description: 'bar'
  }
}

return {
  data: {}
}
```

❌:

```ts
return null

return {
  id: 1,
  name: 'foo',
  description: 'bar'
}

//don't nested data like this...it make no sense unless this belongs to another data object
return {
  data: {
    data: {
      id: 1,
      name: 'foo',
      description: 'bar'
    }
  }
}
```

### For getting array of an entity return:
```ts
interface Response {
  data: Array;
} 
```
Ex: 

✅:

```ts
return {
  data: [
    {
      id: 1,
      name: 'foo',
      description: 'bar'
    },
    {
      id: 2,
      name: 'foo 2',
      description: 'bar 2'
    }
  ]
}

return {
  data: []
}
```

❌:

```ts
return [];

return [
    {
      id: 1,
      name: 'foo',
      description: 'bar'
    },
    {
      id: 2,
      name: 'foo 2',
      description: 'bar 2'
    }
  ]

//don't nested data like this...it make no sense unless this belongs to another data object
return {
  data: {
    data: [
    {
      id: 1,
      name: 'foo',
      description: 'bar'
    },
    {
      id: 2,
      name: 'foo 2',
      description: 'bar 2'
    }
  ]
  }
}
```

### For entity creation and updating return:

Always returned the newly created or updated resource that you got from the DB.

Ex: 

Old object:

```ts
{
  id: 1,
  name: 'foo',
  description: 'bar'
}
```

Object to update:

```ts
{
  id: 1,
  name: 'foo with updated data',
  description: 'bar'
}
```

✅:

```ts
//After updating
return {
  data: {
  id: 1,
  name: 'foo with updated data',
  description: 'bar'
  }
}
```

❌:

```ts
//After updating, should not return old data
return {
  data: {
  id: 1,
  name: 'foo',
  description: 'bar'
  }
}
```


### For query entities data return

```ts
interface Response {
  data: Object;
  metadata: Object;
}
```

Ex: 

✅:

```ts
return {
  data: [
    {
      id: 1,
      name: 'foo',
      description: 'bar'
    },
    {
      id: 2,
      name: 'foo 2',
      description: 'bar 2'
    }
  ],
  metadata: {
    totalPage: 100,
    perPage: 2,
  }
}

return {
  data: [],
  metadata: {
    totalPage: 0,
    perPage: 2,
  }
}

//For implementation this would be using object cursor tail instead of pagination
return {
  data: [
    {
      id: 1,
      name: 'foo',
      description: 'bar'
    },
    {
      id: 23,
      name: 'foo 2',
      description: 'bar 2'
    }
  ],
  metadata: {
    cursor: 23,
    hasMore: true,
  }
}
```

❌:

```ts
return {
  data: [
    {
      id: 1,
      name: 'foo',
      description: 'bar'
    },
    {
      id: 2,
      name: 'foo 2',
      description: 'bar 2'
    }
  ],
  totalPage: 100,
  perPage: 2,
  metadata: {
    hasMore: false
  }
}
```

### For returning multiple additional entities for an entity return

```ts
interface Response {
  data: Object;
  includes: {
    <Entity-Type>: object,
  };
}
```

Ex: 

✅:

```ts
return {
  data: {
    id: 1,
    name: 'foo',
    description: 'bar'
  }
  includes: {
    listings: [
      {
        id: 1,
        name: 'foo listing',
        description: 'bar'
      },
      {
        id: 2,
        name: 'foo listing 2',
        description: 'bar 2'
      }
    ],
    stripeAccount: {
      id: 1,
      paymentMethod: 'card'
    }
  }
}
```

❌:

```ts
return {
  data: {
    id: 1,
    name: 'foo',
    description: 'bar'
  }
  includes: {
    listings: [
      {
        id: 1,
        name: 'foo listing',
        description: 'bar'
      },
      {
        id: 2,
        name: 'foo listing 2',
        description: 'bar 2'
      }
    ],
    //Does not belong to any entity
    id: 1,
    paymentMethod: 'card'
  }
}
```

# Code Modules

## Priorities

Priorities for coding a modules:
1) Readability
2) Reusability
3) Configurable
4) Performance
5) Security
6) Shortness

## Modules

Thumbnail rules for coding everything as module:
- Split your codes into chunks of modules
- A module can `has` multiple modules
- Don't overuse inheritance

### Naming

Biggest modules should be named as an entity, a noun.

Ex:

✅:
`paypal`, `stripe`, `venmo`, `braintree`. 

❌:
Don't use `createPaypal`, `handlingStripe` for outer modules.

Example structure:

✅:
```
modules:
  - paypal:
    - index.js
    - get
    - create
  - stripe:
    - index.js
    - get
    - create
```

Inner layer can use verbs for functions module.

```
modules:
  - paypal:
    - index.js
    - get:
      - index.js
      - fetchData
      - workingOnFoo
      - ticklingBar
    - create
  - stripe:
    - index.js
    - get
    - create
```

❌:
```
modules:
  //Outer layer should not use verbs
  - handlingPaypal:
    - index.js
    - get
    - create
  - stripe:
    - index.js
    - get
    - create
```

### Input

Each module should have a single entry point:
- For `Nodejs` - `index.js`
- For `Deno` - `mod.ts`

Instead of having multiple arguments when calling, everything should be wrapped inside an object so that we do not need to worry about the order of the params.

✅:

```js
const query = ({
  page,
  totalPage
}) => {
  return fetch({
    path: '/api/foo/query',
    queryParams: {
      page,
      totalPage
    }
  });
}

const paypal = {
  query
};

module.exports = paypal;
```

❌:

```js
//Wrap things in object
const query = (page, totalPage) => {
  return fetch({
    path: '/api/foo/query',
    queryParams: {
      page,
      totalPage
    }
  });
}

const paypal = {
  query
};

module.exports = paypal;
```

### Output

The returned data object would the the same as the API response but there must be an additional `status` attributes for each response entity. See more at [api handling error](#handling-errors) and [api response](#handling-response) 

Ex: 

✅:

```ts
return {
  status: 200,
  data: {
    id: 1,
    name: 'foo',
    description: 'bar'
  }
  includes: {
    listings: [
      {
        id: 1,
        name: 'foo listing',
        description: 'bar'
      },
      {
        id: 2,
        name: 'foo listing 2',
        description: 'bar 2'
      }
    ],
    stripeAccount: {
      id: 1,
      paymentMethod: 'card'
    }
  }
}
```

```js
return {
  status: 403,
  name: 'FORBIDDEN',
  data: {
    message: 'Current user is only a normal user, only admin can access this'
  }
}
```

❌:

```ts
//Missing status
return {
  data: {
    id: 1,
    name: 'foo',
    description: 'bar'
  }
  includes: {
    listings: [
      {
        id: 1,
        name: 'foo listing',
        description: 'bar'
      },
      {
        id: 2,
        name: 'foo listing 2',
        description: 'bar 2'
      }
    ],
    stripeAccount: {
      id: 1,
      paymentMethod: 'card'
    }
  }
}
```

## Composing

In backend, our code would be a combination of functional programming and imperative programming. We would favor readability first, so for our code modules, the index file should only for describing what it does instead of giving instruction on what it should do.

✅:

```ts
const handlingPayment = composePromises(
  fetchTransaction,
  validateTransaction,
  createStripeParams,
  stripe.order.create,
  normaliseResponse,
)(paymentParams)
```

❌:

```ts
//This should be split into multiple function instead of writing one big chunk code
const handlingPayment = async (paymentParams) => {
  const {
    transactionId,
    body,
    transition
  } = paymentParams;
  const transactionRes = await axios({
    method: 'GET',
    params: {
      transitionId
    }
  });
  const entities = denormaliseResponseEntity(transactionRes);
  const transaction = entities[0];
  if (!isPendingPayment(transaction)) {
    throw new Error({
      status: 400,
      name: 'INVALID_TRANSITION'
      data: 'INVALID_TRANSITION'
    });
  }
  const stripeParams = {
    lineItems: createStripeLineItems(transaction.attributes.lineItems),
    id: transaction.id.uuid
  }
  const stripeRes = await stripe.order.create(stripeParams);
  const normaliseStripeData = normaliseResponse(stripeRes);
  return {
    status: 200,
    data: normaliseStripeData
  };
}
```

## Comments

Use TODO to tell others what should they do if you intentionally do a dirty code.

✅:

```ts
//TODO: This should be split into multiple function instead of writing one big chunk code
const handlingPayment = async (paymentParams) => {
  const {
    transactionId,
    body,
    transition
  } = paymentParams;
  const transactionRes = await axios({
    method: 'GET',
    params: {
      transitionId
    }
  });
  const entities = denormaliseResponseEntity(transactionRes);
  const transaction = entities[0];
  if (!isPendingPayment(transaction)) {
    throw new Error({
      status: 400,
      name: 'INVALID_TRANSITION'
      data: 'INVALID_TRANSITION'
    });
  }
  const stripeParams = {
    lineItems: createStripeLineItems(transaction.attributes.lineItems),
    id: transaction.id.uuid
  }
  const stripeRes = await stripe.order.create(stripeParams);
  const normaliseStripeData = normaliseResponse(stripeRes);
  return {
    status: 200,
    data: normaliseStripeData
  };
}
```

❌:

```ts
//This should be split into multiple function instead of writing one big chunk code
const handlingPayment = async (paymentParams) => {
  const {
    transactionId,
    body,
    transition
  } = paymentParams;
  const transactionRes = await axios({
    method: 'GET',
    params: {
      transitionId
    }
  });
  const entities = denormaliseResponseEntity(transactionRes);
  const transaction = entities[0];
  if (!isPendingPayment(transaction)) {
    throw new Error({
      status: 400,
      name: 'INVALID_TRANSITION'
      data: 'INVALID_TRANSITION'
    });
  }
  const stripeParams = {
    lineItems: createStripeLineItems(transaction.attributes.lineItems),
    id: transaction.id.uuid
  }
  const stripeRes = await stripe.order.create(stripeParams);
  const normaliseStripeData = normaliseResponse(stripeRes);
  return {
    status: 200,
    data: normaliseStripeData
  };
}
```

## Environments

Should not access `process.env` directly, everything should be access through a `config` modules. We would interact with the `process.env` in the `config` module.

Reason for this is because we would want to have a centralize place for managing existing env on the site. We would not want to be in the situation where whe don't know what kind of env is used on the site.

# Security 

This would be a basic guide, advanced guides would be written later

## Authentication

1) Secrets should never be exposed to clients unless they are for using public sdk. In such cases, secrets should have limited access.
2) Deny first, allow later. Always design system with mindset of denying everyone and gradually open access over time.
3) Should have a single entity verifier instead of having multiple identities for small system to avoid out-of-sync data.
   
   Ex:  In sharetribe flex, instead of creating a new login system for authenticating user to our API request, it's best just to just re-use Flex's existing authentication system.

4) Always verify who the API caller is before doing anything.

## Data

1) `GET` should only return what is asked, do not return more than what it should be 

## Do and Do not (will be regularly updated)




