---
description: 'In this quickstart, you''ll learn how get HyreCar''s GraphQL API up & running'
---

# Quick Start

## Step 1: Clone the Repo

```text
$ git clone https://gitlab.com/hyrecar-dev/backend-v2/services.git
```

{% hint style="warning" %}
We currently use [gitlab](https://gitlab.com) for version control. Access to the repository can be provided by Abhi
{% endhint %}

Once you've cloned repo locally, copy the `.env.sample` file and name it `.env`

{% code-tabs %}
{% code-tabs-item title=".env.sample" %}
```bash
GRAPHQL_ENABLE_MOCKS=false
GRAPHQL_STAGE=dev
GRAPHQL_PRISMA_BASE_URL=https://hyrecar-core_hyrecar.prisma.sh
GRAPHQL_PRISMA_SECRET=mysecret123
GRAPHQL_LEGACY_DB_USERNAME=hyrecar_app
GRAPHQL_LEGACY_DB_PASSWORD=12Udsad34.,oinffsSDmN33Psw12xZ
GRAPHQL_MGMT_AUTH0_CLIENT_SECRET=8WkouXbis288IyhoF18ZJvRa4S9OQ29yc5uM1wf9NEI_eok3kYaOnB3nOTdaX2Ki
GRAPHQL_STRIPE_SECRET_KEY=sk_test_NWkDuiMJYnzIlckWpy1gdVVs
GRAPHQL_S3_SECRET_ACCESS_KEY=1V6PjyVseL/WbLMfDVdKUDIljoF7EORSFYn9KH/f
GRAPHQL_EVENT_GATEWAY_URL=https://hyrecar-hyrecardev.slsgateway.com
GRAPHQL_CHECKR_API_KEY=ZDFjMTBmMWU1NDUxZmI4ZWFiMDBjMzcwYTE0ZDk3NGU1MmYyZTJjYTo=
GRAPHQL_DISABLE_ENGINE=false
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## Step 2: Install Dependencies

Now that you have your environment variables set up, we can now move on to setting up our dependencies to run our gateway server.

{% hint style="danger" %}
Our repo requires yarn workspaces, so please use **yarn** over npm!
{% endhint %}

```text
$ yarn
```

You'll notice that after installing all of our npm package dependencies, that script will also begin to execute some custom scripts. These scripts are essentially packaging up each service \(i.e cars, rentals, and etc.\) into dependencies for our gateway to stitch together and serve.

{% hint style="info" %}
To learn more about this, check out this post here
{% endhint %}

## Step 3: Running the Server

Well, now that we have the repo installed, the environment setup, and our dependencies loaded and ready to go, there's only one thing left!

```bash
$ yarn dev --scope @deployments/gateway
```

This particular script compiles our graphql gateway via a webpack compiler.

{% hint style="info" %}
To learn more about this, check out this post here
{% endhint %}

## Step 4: Making changes

Now that we have the server running, we probably want to make changes to it.

Whenever we make changes to the gateway service, webpack will automatically recompile them. However, we need to perform one additional step if we want to make changes to the users service for example. In a new terminal window, we need to run:

```bash
$ yarn prepare --scope @services/users
```

{% hint style="info" %}
We could also run \`yarn dev --scope @services/users\`, but this will cause a compile loop. We are looking into ways to fix this so we have a better developer experience.
{% endhint %}

## Step 5: Start Exploring!

Once you've got your server up and running, you can start running graphql requests from any graphql IDE!

{% page-ref page="../useful-tools/graphql-ides.md" %}

