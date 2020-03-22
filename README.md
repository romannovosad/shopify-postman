# Shopify Postman

I was looking for a Shopify Postman colleciton and found one done by @lucasxxx and @renatodex, from a couple of years ago. I though I might remove some deprecated features and add OAuth 2.0 authorization.

## How to use?

The Postman Collection file is a JSON containing all information about each request.
This Collection is using Postman Collection Variables, so to adjust them you need to go to the edit collection page and variables tab. Then change "your-development-shop" for your shop name and `api_version` to the version you want to use (don't forget to Reset All).

Now go to authorization tab in the edit collection page and choose **Oauth 2.0** authorization type.

When creating new access token:
- **Callback URL** should be one you whitelisted when creating your Shopify app
- **Auth URL:** `https://{{shop}}.myshopify.com/admin/oauth/authorize`
- **Access Token URL:** `https://{{shop}}.myshopify.com/admin/oauth/access_token`
- **Client ID** and **Client Secret** of your Shopify app
- **Scope:** you can find list of Shopify access scopes [HERE](https://shopify.dev/docs/admin-api/access-scopes)
- **State:** `12345`
- **Client Authentication:** Send client credentials in body

Request your new access token and you should be good to go.

## Missing Endpoints

- Checkout
- User
- UsageCharge
- Draft Order

## Collaboration

Feel free to contribute if you believe there is something missing.


