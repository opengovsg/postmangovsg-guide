# List Messages API

## Overview

{% swagger src="https://api.postman.gov.sg/openapi.yaml" path="/transactional/govsg" method="get" %}
[https://api.postman.gov.sg/openapi.yaml](https://api.postman.gov.sg/openapi.yaml)
{% endswagger %}

## Response format

- `has_more`: a boolean indicating whether there are more emails to retrieve
- `data`: an array of JSON email objects. You can find an example of a single JSON message object [here](./get-message-by-id-api.md).

### Example response

```json
{
  "has_more": false,
  "data": [
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
  ]
}
```
