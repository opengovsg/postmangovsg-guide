# Overview

## Programmatic APIs

Our programmatic APIs allow you to send messages programmatically.&#x20;

### Programmatic email API

We provide a **modern, cost-effective, and compliant PaaS** for sending programmatic emails. Our users include both external agencies, such as ICA, CPF, and MOM, as well as internal OGP products, such as Health Appointment System, Isomer, and CheckWho.

We will launch our programmatic email API officially in Q3 2023. Interested users can reach out to us via [this form](https://form.gov.sg/62b19812ff209e00126f2c47).&#x20;

To illustrate how our programmatic email API works, when an applicant submits a grant on your website, you can configure your system to call our API to send out an acknowledgement email. The same can be done for sending OTPs, emails confirming appointment booking, status update emails and so on.

### Programmatic SMS API

\[This section is under construction]

## Campaign API

Our Campaign APIs are meant to support our users who access us via the frontend on PostmanSG and are not designed to be accessed programmatically and thus might be modified without prior notice. You may find their endpoints in our [Swagger Docs](https://api.postman.gov.sg/docs/). As such, we recommend that you <mark style="background-color:yellow;">speak with us</mark> regarding your use case before using these APIs.

{% hint style="info" %}
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
