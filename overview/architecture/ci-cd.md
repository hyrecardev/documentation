---
description: The deployment flow
---

# CI/CD

## Overview

We use gitlab CI to manage the deployment of the server. There are two main steps that take place:

1. Build the docker images and push them to AWS ECR
2. Deploy the services to AWS Elastic Beanstalk as well as zeit now.sh

The servers deployed to Elastic Beanstalk are what are available for the frontend apps via [https://api.hyrecar.com](https://api.hyrecar.com) and [https://internal-api.hyrecar.com](https://internal-api.hyrecar.com).

### Deployment Steps

I will show the steps for deploying the staging server. We follow the same steps for the production server, but it will only be available on the master branch.

### Step 1.1: Build

![](../../.gitbook/assets/screen-shot-2018-08-15-at-12.23.12-pm.png)

### Step 1.2: Deploy now.sh

![](../../.gitbook/assets/screen-shot-2018-08-15-at-12.26.52-pm.png)

### Step 2: Deploy to internal and public servers

![](../../.gitbook/assets/screen-shot-2018-08-15-at-12.26.52-pm.png)



