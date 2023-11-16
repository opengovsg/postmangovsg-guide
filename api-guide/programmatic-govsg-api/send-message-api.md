# Send Message API

{% hint style="warning" %}
**Updated 25 October 2023** We have stopped onboarding new agencies to the Gov.sg WhatsApp channel
{% endhint %}

## Overview

This endpoints accept a request body that contains information about the Gov.sg WhatsApp message to be sent. Each successful request to this endpoint will send out a single Gov.sg WhatsApp message.

{% swagger src="https://api.postman.gov.sg/openapi.yaml" path="/transactional/govsg/send" method="post" %}
[https://api.postman.gov.sg/openapi.yaml](https://api.postman.gov.sg/openapi.yaml)
{% endswagger %}

## Request Body

1.  `recipient`: Mobile phone number of the recipient without special formatting (only contains numerical characters and prefixed with plus sign if country code is included).

    **Notes**:

    * Country code will need to be provided for non-SG mobile numbers.
    * If country code is not provided, the phone number will be defaulted to be an SG number.
2. `template_id`: ID of the template that suits your need (can be retrieved from [GET templates endpoint](get-templates-api.md))
3. `params`: A key-value object with keys being the parameter names (wrapped in double curly braces in the template body) and corresponding string values to fill in the template body.
4. `language_code` (optional): The language code that can be retrieved from the `multilingual_support` field of the template

## API Response

For general information about our API response formats, [see here](../../overview/api-response-formats.md).

### Example Response

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
  "updated_at": "2023-07-31T16:40:01.526Z",
  "accepted_at": "2023-07-31T16:40:01.526Z",
  "sent_at": null,
  "delivered_at": null,
  "read_at": null,
  "errored_at": null,
  "error_code": null,
  "error_description": null,
  "status": "ACCEPTED"
}
```

{% hint style="info" %}
For message status, we have 6 different states that a message can be in:

* `UNSENT` - Initial state of a newly created transactional Gov.sg message (this status is not returned in the course of a successful request to send a GovSG message)
* `ACCEPTED` - Message has been accepted by our service provider (this status is returned in the course of a successful request to send a Gov.sg message)
* `SENT` - The send request was successfully forwarded to our service provider and our service provider will attempt to deliver the message to the recipient’s phone number (API user can check this and all subsequent statuses via the `/transactional/govSG/{messageId}` endpoint)
* `DELIVERED` - The service provider has successfully delivered the message to the recipient's phone number
* `READ` - The recipient has received the message and viewed it
* `ERROR` - An error happened when the service provider is trying to deliver the message
{% endhint %}
