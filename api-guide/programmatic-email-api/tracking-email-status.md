# Tracking Email Status

API users can track the status of emails sent via our API.

{% hint style="info" %}
We rely on Amazon SES's event tracking to update the status of emails sent via our API. This means that the status of emails sent via our API may not be updated in real-time and, depending on the settings of the recipient's email provider, this event tracking may be skewed. As such, the accuracy of our email status tracking is not guaranteed. For more information, please refer to [this page](https://docs.aws.amazon.com/ses/latest/dg/faqs-metrics.html).
{% endhint %}

## Email Status

You can get the status of each email sent sent using [this API endpoint](./get-email-by-id-api.md).

We currently do not support pushing webhooks to your server when the status of an email changes. We are exploring the possibility of providing more email analytics, such as monthly reports aggregating statistics about email deliverability grouped based on user-defined tags. For more information, see [this section](./send-email-api/email-tagging-and-classification.md).

For a list of statuses supported by our API, please refer to the table below.

| Status      | Definition                                                                                                                                                                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `UNSENT`    | Initial state of a newly created transactional email (this status is not returned in the course of a successful request to send an email)                                                                                                                           |
| `ACCEPTED`  | Email has been accepted by our email provider (this status is returned in the course of a successful request to send an email)                                                                                                                                      |
| `SENT`      | The send request was successfully forwarded to our email provider and our email provider will attempt to deliver the message to the recipient’s mail server (API user can check this and all subsequent statuses via the `/transactional/email/{emailId}` endpoint) |
| `BOUNCED`   | The recipient's mail server rejected the email                                                                                                                                                                                                                      |
| `DELIVERED` | The email provider has successfully delivered the email to the recipient's mail server                                                                                                                                                                              |
| `OPENED`    | The recipient received the message and opened it in their email client                                                                                                                                                                                              |

## Error Codes and Error Subtype

The `errorCode` and `errorSubType` fields in the JSON object returned [by our API](./get-email-by-id-api.md) supplement the email status and provide additional information.

You can find a non-exhaustive list of error codes below.

### Error code while sending emails

1. Invalid from address: the user has entered a from address that is neither their own (the email address used to log into Postman) nor `<donotreply@mail.postman.gov.sg>`.
2. From address has not been verified: the user should contact the Postman team to verify their from address.
3. Blacklisted recipient: the recipient's email address is on our blacklist. For more information, see [this section](./send-email-api/recipient-blacklist.md).

### Error code after an email has been sent

1. Hard bounce: the recipient's mail server permanently rejected the email (e.g. the recipient's email address does not exist).
2. Soft bounce: the recipient's mail server temporarily rejected the email (e.g. the recipient's mailbox is full).
3. Complaint: the recipient has marked the email as spam.

For the error codes above, you can find more information by checking the `errorSubType` field.

## Tracking Open Rates

To track open rates of emails, a 1 pixel by 1 pixel transparent GIF image is inserted in each email sent through Amazon SES and includes a unique reference to this image file; when the image is downloaded, SES can tell exactly which message was opened and by whom. In general, the addition of this tracking pixel does not change the appearance of your email. However, for Intranet recipients, this tracking pixel might be blocked and show up as a red cross. Currently, we do not support opting out of this tracking pixel.

For more information, you can refer to [this page](https://docs.aws.amazon.com/ses/latest/dg/faqs-metrics.html).
