# 📨 Programmatic Email API

We provide a **modern, cost-effective, and compliant PaaS** for to send programmatic emails.

## What are programmatic emails?

These are emails that are triggered by a computer system, typically as part of a larger workflow.

For example, consider an agency that receives grant applications from members of the public. When an applicant submits a grant on your website, upon receiving the submission, your system could call our API to send out an acknowledgement email. The same could be done for sending one-time-passwords (OTPs), appointment booking confirmations, status updates emails, and so on.

Our existing users include both external agencies, such as ICA, CPF, and MOM, as well as OGP products, such as [Health Appointment System](https://book.health.gov.sg/), [Isomer](https://www.isomer.gov.sg/), [CheckWho](https://checkwho.gov.sg/login), and [Care360](https://care360.health.gov.sg/login).

## Value proposition

Our product is built on top of the commercial cloud and thus is aligned with the Government's "Commercial Cloud First Policy" to unlock the benefits of the cloud, such as improved reliability, auto-scaling, and lower costs.

For Intranet users, our API is most similar to App Mail Relay (AMR). For more details:

* [IM8 Policies](../overview/im8-policies.md)
* [Comparison with AMR](comparison-with-amr.md)

For Internet users:

* By using our PaaS service allows you to abstract away the undifferentiated heavy lifting of setting up and maintaining your own email sending system, allowing you to focus on your core business logic.
* Compared to commercial PaaS, our product is free for government agencies to use and is set up to ensure deliverability to SG-Mail recipients.

## Feature list

* Modern, cloud-native, self-serve
* Free. No GeBiz purchase order to submit, no billing or invoices to deal with.
* [IM8-compliant](../overview/im8-policies.md)
  * As a product of [Open Government Products](https://www.open.gov.sg/), we are exempt from IM8 policies.
  * Nonetheless, we strive to build our policies in a manner that is consistent with SNDGO's Cloud Security Policy.
* [Attachments](send-email-api/attachments.md)
* [Custom domain](custom-from-address.md)
* [Email tagging and classification](send-email-api/email-tagging-and-classification.md)
* [Tracking email status](tracking-email-status.md)
* Endpoints for [querying email](get-email-by-id-api.md) and [listing emails](list-emails-api.md)
* [SG-Mail whitelisting](sg-mail-whitelisting.md) to ensure delivery to Intranet recipients
* [Multiple API keys for regular key rotation](../api-key-management/)
* Rolling deployment with zero downtime

## Express interest and FAQs

{% hint style="warning" %}
**Updated 26 September 2023:** Postman will no longer be onboarding any new programmatic email API user till further notice.
{% endhint %}

If you have any queries, you can check out this [API FAQ page](../frequently-asked-questions.md).
