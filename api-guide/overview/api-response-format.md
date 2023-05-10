---
description: Handling responses from the Postman API
---

# API Response Formats

## HTTP Status Codes

Postman uses conventional API Responses Codes to indicate the success or failure of an API request.

{% hint style="info" %}
Sending messages is an asynchronous process. As such, a successful API request to our message sending endpoints simply mean the request has been made successfully. It does not mean that your message has been sent or delivered successfully. To check this, you should call the respective endpoints ([email](../programmatic-email-api/email-status-api.md), [SMS](../programmatic-sms-api.md)) to check the status of your message.
{% endhint %}

| Code                         | Description                                                                                                                                                                                       |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 200 - OK                     | Everything worked as expected                                                                                                                                                                     |
| 201 - Created                | Resource created. The message is being sent.                                                                                                                                                      |
| 202 - Accepted               | We have accepted the request, but processing has not been completed. This is usually used for long-running processes like handling uploads of recipient lists to generate messages for campaigns. |
| 400 - Bad Request            | The request was unacceptable, often due to missing a required parameter or parameter supplied in an incorrect format.                                                                             |
| 401 - Unauthenticated        | Invalid API key provided.                                                                                                                                                                         |
| 403 - Forbidden              | User doesn't have permission to perform the request, could be due to resources are in an invalid state for the operation.                                                                         |
| 404 - Not Found              | The requested resource doesn't exist.                                                                                                                                                             |
| 410 - Gone                   | Data has been redacted from Postman.                                                                                                                                                              |
| 413 - Content Too Large      | Number of attachments or size of attachments exceeded limit.                                                                                                                                      |
| 429 - Too Many Requests      | Rate limit exceeded. Too many requests.                                                                                                                                                           |
| 500 - Internal Server Error. | Something went wrong on Postman's end. (These are rare.)                                                                                                                                          |

## Format of Successful Responses

All responses to successful requests to the Postman API will be returned in JSON format with a HTTP status code in the `2xx` range. The response will contain information about the resources that are being acted on (e.g. creation, retrieval). The following is an example of a JSON object received after sending an email via the [programmatic email API](../programmatic-email-api/):

```json
{
  "id": "42",
  "from": "Postman <donotreply@mail.postman.gov.sg>",
  "recipient": "hello@example.com",
  "params": {
    "body": "Hello World",
    "from": "Postman <donotreply@mail.postman.gov.sg>",
    "subject": "Hello World",
    "reply_to": "hello@example.com"
  },
  "attachments_metadata": [
    {
      "fileName": "example.pdf",
      "fileSize": 1240,
      "hash": "8743b52063cd84097a65d1633f5c74f5"
    }
  ],
  "status": "ACCEPTED",
  "error_code": null,
  "error_sub_type": null,
  "created_at": "2023-05-10T03:03:55.406Z",
  "updated_at": "2023-05-10T03:03:55.406Z",
  "accepted_at": "2023-05-10T03:03:55.406Z",
  "sent_at": null,
  "delivered_at": null,
  "opened_at": null,
  "classification": "FOR_ACTION",
  "tag": "hello world"
}
```

## Format of Error Responses

For error responses (with non-`2xx` codes),  the response will be in JSON format with these fields

```json
{
  "code": "error code for this specific error type",
  "message": "human-readable explanation of the error and possibly the next step"
}
```

Ideally, most of our errors are expected to happen during development process for your system and to serve as guidelines for your developers. However, some might happen for your production system (for e.g. `429 rate_limit` error), in which case, using the `code` field is a reliable way to programmatically handle those error flows. All error `code`(s) can be found in [our Swagger documentation ](https://api.postman.gov.sg/docs)or under the respective sections of this guide.

