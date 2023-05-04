# Email Status API

{% hint style="warning" %}
This page is under construction.
{% endhint %}

You can get the delivery status of the emails sent using the `GET`endpoint `/transactional/email`.\
\
Below is a list of statuses you might receive and what it means.

| Status      | Definition                                                                                                                                                                                                                                                          |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `UNSENT`    | initial state of a newly created transactional email (this status is not returned in the course of a successful request to send an email)                                                                                                                           |
| `ACCEPTED`  | email has been accepted by our email provider (this status is returned in the course of a successful request to send an email)                                                                                                                                      |
| `SENT`      | the send request was successfully forwarded to our email provider and our email provider will attempt to deliver the message to the recipient’s mail server (API user can check this and all subsequent statuses via the `/transactional/email/{emailId}` endpoint) |
| `BOUNCED`   | the recipient's mail server rejected the email                                                                                                                                                                                                                      |
| `DELIVERED` | the email provider has successfully delivered the email to the recipient's mail server                                                                                                                                                                              |
| `OPENED`    | the recipient received the message and opened it in their email client                                                                                                                                                                                              |
