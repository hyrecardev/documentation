---
description: >-
  Each directory in the packages and services folders is a self-contained
  repository with its own dependencies and configuration. These services can be
  used as npm dependencies by other services.
---

# Organization

## Packages

The `packages` directory is intended for utilities and tooling to be used by the packages in the services directory. As of this writing, the only "package" we have is `service-utils` which is a store of general utilities to be used throughout the monorepo.

## Services

The services directory is intended for API code. This is where we keep the packages for the users, cars, rentals, etc. 

### Users, Cars, Rentals, etc.

The directories which are named by business function are self-contained graphql schemas. Each of these services have their own database configured via the prisma graphql layer and a schema which extends the database. Each service generate a graphql binding and provides a typed SDK to be used by the gateway. Graphql bindings are what enable us to do this:

```typescript
const user = await context.users.query.user( { where: { id: userId, }, }, "{ id firstName }", { context } ) 
```

### Gateway

The gateway is our API server. It is the glue which binds all of the other services together. It determines how, say, the users schema relates to the files schema. We use what is called schema stitching to accomplish this.

{% page-ref page="../../concepts/schema-stitching.md" %}

Since each of the business-specific services only handle logic specific to its area of the business, the gateway will orchestrate the business logic across the services. For example, when a driver requests to book a car, it spans across the users, cars, rentals and payments services. The gateway will handle which order to perform each operation.

You can learn more about how the server is configured here:

{% page-ref page="../graphql-server-graphql-yoga-apollo-server.md" %}

