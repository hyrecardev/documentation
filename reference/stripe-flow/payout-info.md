---
description: How the owner enters their payout information to receive payments.
---

# Payout Info

To update a user's Payment information, we use the `updatePayoutInfo` mutation. This mutation expects a stripe `accountToken` and `bankToken` generated on the client side.

### accountToken:

{% embed data="{\"url\":\"https://stripe.com/docs/connect/account-tokens\",\"type\":\"link\",\"title\":\"Using Account Tokens\",\"description\":\"Online payment processing for internet businesses. Stripe is a suite of payment APIs that powers commerce for businesses of all sizes.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://stripe.com/img/apple-touch-icon/180x180.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://stripe.com/img/v3/home/social.png\",\"width\":1024,\"height\":512,\"aspectRatio\":0.5}}" %}

### bankToken:

{% embed data="{\"url\":\"https://stripe.com/docs/stripe-js/reference\#collecting-bank-account-details\",\"type\":\"link\",\"title\":\"Stripe.js Reference\",\"description\":\"Online payment processing for internet businesses. Stripe is a suite of payment APIs that powers commerce for businesses of all sizes.\",\"icon\":{\"type\":\"icon\",\"url\":\"https://stripe.com/img/apple-touch-icon/180x180.png\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://stripe.com/img/v3/home/social.png\",\"width\":1024,\"height\":512,\"aspectRatio\":0.5}}" %}

