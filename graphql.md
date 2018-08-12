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

Once you've cloned repo locally, rename the `.env.sample` file to `.env]`

{% code-tabs %}
{% code-tabs-item title=".env.sample" %}
```text
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
GRAPHQL_CHECKR_API_KEY="ZDFjMTBmMWU1NDUxZmI4ZWFiMDBjMzcwYTE0ZDk3NGU1MmYyZTJjYTo="
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

```text
$ yarn dev --scope @deployments/gateway
```

This particular script compiles our graphql gateway via a webpack compiler.

{% hint style="info" %}
To learn more about this, check out this post here
{% endhint %}

## Step 4: Start Exploring!

Once you've got your server up and running, you can start making running graphql requests from any graphql IDE!

