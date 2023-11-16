# Bearer Authentication

## About Bearer Authentication

Bearer authentication (also called token authentication) is a HTTP authentication scheme that involves security tokens called bearer tokens. Note that bearer authentication should only be used over HTTPS (SSL). For more information, [see here](https://swagger.io/docs/specification/authentication/bearer-authentication/).

In the rest of this guide, we will use "API key" to refer to the bearer token used for authentication.

## Authentication Header

Postman uses bearer authentication. In practice, this means that clients calling our API should include the API key in the `Authorization` header when making requests:

```http
Authorization: Bearer <api_key>
```
