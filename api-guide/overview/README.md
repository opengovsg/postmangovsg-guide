# Overview

## Programmatic APIs

Our programmatic APIs allow you to send messages programmatically.&#x20;

### Programmatic Email API

We provide a **modern, cost-effective, and compliant PaaS** for to send programmatic emails.&#x20;

We will launch our programmatic email API officially in Q3 2023. Interested users can reach out to us via [this form](https://go.gov.sg/postmanp-api-wogict).

{% hint style="info" %}
To illustrate an agency might use our programmatic email API, consider an agency that receives grant applications from members of the public. When an applicant submits a grant on your website, instead of configuring your own email sending system, you could configure your system to call our API to send out an acknowledgement email.  The same could be done for sending one-time-passwords (OTPs), appointment booking confirmations, status updates emails, and so on.
{% endhint %}

To find out more, click [here](https://guide.postman.gov.sg/api-guide/programmatic-email-api).

### Programmatic SMS API

{% hint style="warning" %}
This section is under construction
{% endhint %}

## Campaign API

Our Campaign APIs are meant to support our users who access us via the frontend on PostmanSG and are not designed to be accessed programmatically and thus might be modified without prior notice. You may find their endpoints in our [Swagger Docs](https://api.postman.gov.sg/docs/). As such, we recommend that you <mark style="background-color:yellow;">speak with us</mark> regarding your use case before using these APIs.

{% hint style="danger" %}
Please note the following limitations with our campaign API endpoints:

* Password protected campaigns are not supported
* These endpoints might be modified without prior notice

_If you have additional enquiries or potential use cases using the Campaigns API, please_ [_contact us_](https://go.gov.sg/postman-contact-us)_._
{% endhint %}

## Programmatic API vs Campaign API

| Type                   | Programmatic API                                         | Campaign API                                             |
| ---------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| **How it works**       | Sends to one recipient at a time                         | Bulk sends to multiple recipients at once                |
| **Examples use cases** | Application approval, OTP, email receipt, reminders etc. | Mass event invitation, mass broadcast of a policy update |
