# Get Email by ID API

This API allows you to retrieve metadata about a specific email sent via our API via its `id`. The most common use case for this API is to check on the status of an email.

## How It Works

{% hint style="info" %}
To use this API, you must save the `id` field in the response returned when making an API call to send the email. For more information, see [this section](./send-email-api/README.md#response-json-object).
{% endhint %}

{% swagger src="https://api.postman.gov.sg/openapi.yaml" path="/transactional/email/{emailId}" method="get" %}
[https://api.postman.gov.sg/openapi.yaml](https://api.postman.gov.sg/openapi.yaml)
{% endswagger %}

## Example Response

```json
{
  "id": "42",
  "from": "Postman.gov.sg <donotreply@mail.postman.gov.sg>",
  "recipient": "hello@example.com",
  "params": {
    "body": "Hello World",
    "from": "Postman.gov.sg <donotreply@mail.postman.gov.sg>",
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
  "status": "DELIVERED",
  "error_code": null,
  "error_sub_type": null,
  "created_at": "2023-05-10T03:03:54.163Z",
  "updated_at": "2023-05-10T03:05:00.000Z",
  "accepted_at": "2023-05-10T03:03:55.406Z",
  "sent_at": "2023-05-10T03:04:01.912Z",
  "delivered_at": "2023-05-10T03:05:00.000Z",
  "opened_at": null,
  "classification": "FOR_ACTION",
  "tag": "hello world"
}
```

## Limitations

We currently do not support pushing webhooks to your server when the status of an email changes. We are exploring the possibility of providing more email analytics, such as monthly reports aggregating statistics about email deliverability grouped based on user-defined tags. For more information, see [this section](./send-email-api/email-tagging-and-classification.md).
