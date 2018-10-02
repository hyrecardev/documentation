---
description: Overview of package maintenance for the services repo.
---

# Maintenance

There are a few key packages in the services monorepo which we need to keep updated.

## Root Packages

### \*[prisma](https://github.com/prisma/prisma) \(current: v1.7.3\)

[https://www.prisma.io/docs/maintain/](https://www.prisma.io/docs/maintain/)

### [typescript](https://github.com/Microsoft/TypeScript) \(current: v2.8.3\)

## Service Packages

Service-level packages are packages installed on each individual packages. If we need to upgrade these, we need to upgrade on each service.

### \*[prisma-binding](https://github.com/prisma/prisma-binding) \(current: v2.0.1\)

### [graphql-binding](https://github.com/graphql-binding/graphql-binding) \(current: 2.1.0\)

### [graphql](https://github.com/graphql/graphql-js) \(current: v0.13.2\)

## 3rd Party Services

### [api2pdf](https://www.api2pdf.com/)

Used to generate pdfs of rental contracts. We setup up auto payment, but it is a good idea to keep an eye on this once in a while to make sure the payment balance is above $0.

