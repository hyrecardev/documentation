---
description: An overview of each elastic beanstalk deployment and what it is.
---

# Elastic Beanstalk Deployments

## graphql-rest-wrapper

This application is what hosts the graphql apis. We currently have staging and production environments under this application.

### hyrecar-api-v2-\[staging-\]\[internal \| public\]

The main GraphQL APIs one for the internal api and another for public.

### hyrecar-graphql \(deprecated\)

This was the previous graphql server which was wrapping the legacy REST API. We no longer use this endpoint. We will need to remove it in the near future.



## ManageAndAPI

This application is what hosts the legacy REST API and manage servers. It contains both staging and production environments.

### hyrecar-\[manage2 \| api2\]-\[production \| staging\]

These are the main servers which host the legacy REST API. 

{% hint style="danger" %}
We currently still rely on the cars and states db, so we should make sure not to take these servers down until we migrate completely.
{% endhint %}



