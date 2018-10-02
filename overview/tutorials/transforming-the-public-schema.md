---
description: We can modify the schema to remove fields that are unnecessary for our api.
---

# Transforming the Public Schema

## Overview

Schema transforms let us modify the schema before it becomes visible to the public. We currently implemented schema transforms only for the public version of the server since it is completely exposed. The internal version exposes everything since it requires authentication to access any of it.

{% hint style="danger" %}
We must be careful not to break existing clients by doing these transforms. So, if you need to be hiding specific fields, please make sure to test the existing clients. If this is becoming a recurring problem, we can implement [Apollo Engine's Schema History](https://www.apollographql.com/docs/engine/features/schema-history.html) feature.
{% endhint %}

### Use Cases

* We want to hide sensitive fields for security purposes.
* We want to reduce the number of arguments for where args.

## Tutorial

Transforming the schema is a very straightforward process.

### Step 1: Navigate to the transforms file

Located in:

`services/gateway/src/publicServer/schemaTransforms.ts`

### Step 2: Add or modify parts of the schema

We have two main parts of the schema transformed; the Query and the Mutation. You can learn more about how schema transforms work here:

{% embed data="{\"url\":\"https://github.com/prisma/graphql-transform-schema\",\"type\":\"link\",\"title\":\"prisma/graphql-transform-schema\",\"description\":\"Transform, filter & alias resolvers of a GraphQL schema - prisma/graphql-transform-schema\",\"icon\":{\"type\":\"icon\",\"url\":\"https://github.com/fluidicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://avatars3.githubusercontent.com/u/17219288?s=400&v=4\",\"width\":400,\"height\":400,\"aspectRatio\":1}}" %}

### Example

Lets go over an example of how to reduce the number of arguments on the `cars` `where` args in the query:

You will notice in the schema explorer on the Graphql Playground that the cars query's where args type is called `CarWhereInput`, so we add an attribute with the same name to the exported object. We can transform the schema in one of two ways:

By excluding specific fields:

{% code-tabs %}
{% code-tabs-item title="schemaTransforms.ts" %}
```typescript
export default {
  ...
  Query: {
    ...

  },
  Mutation: {
    ...
  },
  CarWhereInput: {
    'createdAt': false,
    'photos*': false,
  }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Or by disabling all fields and enabling specific ones:

{% code-tabs %}
{% code-tabs-item title="schemaTransforms.ts" %}
```typescript
export default {
  ...
  Query: {
    ...

  },
  Mutation: {
    ...
  },
  CarWhereInput: {
    '*': false
    'id': true,
    'photos*': true,
  }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

