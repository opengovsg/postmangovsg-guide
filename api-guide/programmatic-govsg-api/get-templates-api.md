# Get Available Templates API

## Overview

This endpoint returns information about the available message templates for your account that can be used to send out Gov.sg WhatsApp messages.

{% swagger src="https://api.postman.gov.sg/openapi.yaml" path="/govsg/templates" method="get" %}
[https://api.postman.gov.sg/openapi.yaml](https://api.postman.gov.sg/openapi.yaml)
{% endswagger %}

## API Response

For general information about our API response formats, [see here](../../overview/api-response-formats.md).

### Example Response

```json
{
  "data": [
    {
      "id": 1,
      "body": "<b>From</b>: {{ agency }}\n<b>Subject</b>: Upcoming phone call\n\nDear {{ recipient_name }},\nWe will be calling you today between {{ timeslot }} about {{ topic }}. We request your availability during this period.\n\nSincerely,\n{{ officer_name }}\n{{ officer_designation }}\n{{ agency }}\n\n<i>This is an automated message. Please do not reply.</i>",
      "params": [
        "agency",
        "recipient_name",
        "timeslot",
        "topic",
        "officer_name",
        "officer_designation"
      ],
      "param_metadata": {
        "topic": {
          "displayName": "Topic"
        },
        "agency": {
          "defaultFromMetaField": "agency"
        },
        "timeslot": {
          "displayName": "Timeslot"
        },
        "officer_name": {
          "defaultFromMetaField": "officer_name"
        },
        "recipient_name": {
          "displayName": "Recipient Name"
        },
        "officer_designation": {
          "defaultFromMetaField": "officer_designation"
        }
      },
      "name": "Notify users of an upcoming call",
      "multilingual_support": [
        {
          "languageCode": "zh_CN",
          "language": "Chinese",
          "body": "<b>From</b>: {{ agency }}\n<b>Subject</b>: Upcoming phone call\n\nDear {{ recipient_name }},\nWe will be calling you today between {{ timeslot }} about {{ topic }}. We request your availability during this period.\n\nSincerely,\n{{ officer_name }}\n{{ officer_designation }}\n{{ agency }}\n\n<i>This is an automated message. Please do not reply.</i>"
        }
      ]
    }
  ]
}
```

{% hint style="info" %}
The`id` and `languageCode` fields will be used in the [sending endpoint]() later to indicate the specific template and lingual variation that you want to send your message out using.
{% endhint %}
