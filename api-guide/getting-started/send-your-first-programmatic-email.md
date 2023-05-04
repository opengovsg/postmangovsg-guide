# Send your first programmatic email

{% hint style="warning" %}
This page is under construction.
{% endhint %}

Without attachments

```zsh
curl --location --request POST 'https://api.postman.gov.sg/v1/transactional/email/send' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer your_api_key' \
--data-raw '{
  "subject": "Test email",
  "body": "<p>Hello <b>there</b></p>",
  "recipient": "user@agency.gov.sg"
}'
```
