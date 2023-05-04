# API Response Format

{% hint style="warning" %}
This page is under construction.
{% endhint %}

Postman uses conventional API Responses Codes to indicate the success or failure of an API request.

{% hint style="info" %}
Response codes do not tell you the delivery status or if your emails are sent. You should be calling the [status](https://api.postman.gov.sg/docs/#/Email/get\_transactional\_email) endpoint.
{% endhint %}

| Code | Description                                                                                                                                                                                        |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 201  | Created. The message is being sent.                                                                                                                                                                |
| 400  | Bad Request. Failed parameter validations, message is malformed, or attachments are rejected.                                                                                                      |
| 401  | Unauthorised                                                                                                                                                                                       |
| 403  | Forbidden. Request violates firewall rules.                                                                                                                                                        |
| 413  | Number of attachments or size of attachments exceeded limit.                                                                                                                                       |
| 429  | Rate limit exceeded. Too many requests.                                                                                                                                                            |
| 500  | <p>Internal Server Error.<br>This includes error such as custom domain passed email validation but is incorrect; see <a href="https://github.com/opengovsg/postmangovsg/issues/1837">here</a>.</p> |
