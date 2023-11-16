# Tracking Message Status

API users can track the status of messages sent via our API.

## Gov.sg WhatsApp Message Status

You can get the status of each email sent sent using [this API endpoint](tracking-message-status.md).

We currently do not support pushing webhooks to your server when the status of a message changes.

For a list of statuses supported by our API, please refer to the table below.

| Status      | Definition                                                                                                                                                                                                                                                                 |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `UNSENT`    | Initial state of a newly created transactional Gov.sg message (this status is not returned in the course of a successful request to send a Gov.sg message)                                                                                                                 |
| `ACCEPTED`  | Message has been accepted by our service provider (this status is returned in the course of a successful request to send a Gov.sg message)                                                                                                                                 |
| `SENT`      | The send request was successfully forwarded to our service provider and our service provider will attempt to deliver the message to the recipient’s phone number (API user can check this and all subsequent statuses via the `/transactional/govSG/{messageId}` endpoint) |
| `DELIVERED` | The service provider has successfully delivered the message to the recipient's phone number                                                                                                                                                                                |
| `READ`      | The recipient has received the message and viewed it                                                                                                                                                                                                                       |
| `ERROR`     | An error happened when the service provider is trying to deliver the message                                                                                                                                                                                               |

## Error Codes and Error Description

The `error_code` and `error_description` fields in the JSON object returned [by our API](tracking-message-status.md) supplement the email status and provide additional information.

You can find a non-exhaustive list of error codes below.

### Error code while attempting to send messages

* `invalid_recipient`: This error is returned when the recipient number provided is either not a valid phone number or doesn't have any WhatsApp account associated with it. Under this scenario, no message will be sent out.

### Error code after a message has been sent

After Postman platform has successfully forwarded the message request to our provider WhatsApp, all errors that are logged from WhatsApp will be recorded in Postman system with the corresponding `error_code` and human-readable `error_description`.

For more details about the possible errors that can happen, please check out [this page](https://developers.facebook.com/docs/whatsapp/cloud-api/support/error-codes/#error-codes).

## Tracking open rates

A message is recorded as `READ` when the recipient has opened the thread and blue-ticked the message. Please note that if the recipient configure their WhatsApp to not send read receipt, this won't happen hence the message status will finalise at `DELIVERED`.
