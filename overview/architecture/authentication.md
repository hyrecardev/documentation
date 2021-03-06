---
description: An overview of the authentication flow.
---

# Authentication Flow

![We need to digitize this](../../.gitbook/assets/img_20180815_111648.jpg)

## Auth0

Auth0 is primarily responsible for our security. It authenticates the users and issues the JWT tokens for our frontend clients to make authenticated requests to our APIs.

{% embed data="{\"url\":\"https://auth0.com/docs\",\"type\":\"link\",\"title\":\"Auth0 Docs\",\"description\":\"Get started using Auth0. Implement authentication for any kind of application in minutes.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://cdn2.auth0.com/styleguide/latest/lib/logos/img/favicon.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://cdn2.auth0.com/docs/media/social-media/fb-card.png\",\"width\":1200,\"height\":630,\"aspectRatio\":0.525}}" %}

### Rules

We primarily use Auth0 rules to enrich the customer profile for when they sign up as well as to retrieve basic user data to include as part of the JWT payload. These rules are deployed via the Gitlab plugin on Auth0 to sync any changes in the repo on the staging and production branches to their respective tenant. 

## Graphql Server

When a request hits our server, it will go through the following middleware before reaching the graphql API code:

### Step 1: Validate the JWT token

The `express-jwt` plugin validates the JWT token sent by our frontend clients and adds a `user` attribute with the token's payload to the express request object.

### Step 2: Get `currentUser`

This middleware will use the `user` attribute exposed from step 1 and:

* If user details are included in the payload, it exposes that as the `currentUser`.
* If no user data is in the payload, it will retrieve the user from our database by their Auth0 userId \(which we store as part of the user table\) or email address and returns that as the `currentUser`.
* If no such user exists, then it is a new user. We fetch additional user details directly from Auth0 \(which has their enriched profile data\) and add them to our database and return the newly created user as `currentUser`.

### Step 3: Check scopes \(internal server only\)

For the Internal API endpoint, we can receive two types of tokens \(machine-to-machine or normal user\). In either case, this middleware checks the scopes or user roles to make sure they have the appropriate permissions.

### Step 4: Execute schema code

Once the above steps are completed, the request will hit the graphql api code. The `getContext` method will receive the express request with the pre-populated `currentUser` attribute and injects it into the graphql context to be used throughout the schema.

