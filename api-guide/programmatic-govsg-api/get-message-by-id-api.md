# Get Message by ID API

This API allows you to retrieve metadata about a specific message sent via our API via its `id`. The most common use case for this API is to check on the status of a message.

## How It Works

{% hint style="info" %}
To use this API, you must save the `id` field in the response returned when making an API call to send the Gov.sg message.
{% endhint %}

{% swagger src="https://api.postman.gov.sg/openapi.yaml" path="/transactional/govsg/{messageId}" method="get" %}
[https://api.postman.gov.sg/openapi.yaml](https://api.postman.gov.sg/openapi.yaml)
{% endswagger %}

## Example Response

```json
{
  "id": "505",
  "recipient": "+6581489408",
  "template_id": "1",
  "params": {
    "topic": "document collection",
    "agency": "Open Government Products",
    "timeslot": "1-3PM",
    "officer_name": "John Tan",
    "recipient_name": "Stanley Nguyen",
    "officer_designation": "Reception Officer"
  },
  "language_code": "en_GB",
  "created_at": "2023-07-31T16:39:59.631Z",
  "updated_at": "2023-07-31T16:40:02.558Z",
  "accepted_at": "2023-07-31T16:40:01.526Z",
  "sent_at": "2023-07-31T16:40:01.000Z",
  "delivered_at": "2023-07-31T16:40:02.000Z",
  "read_at": null,
  "errored_at": null,
  "error_code": null,
  "error_description": null,
  "status": "DELIVERED"
}
```
