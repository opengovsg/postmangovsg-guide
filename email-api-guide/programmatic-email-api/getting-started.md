---
description: >-
  This page gives you an overview of what to expect when onboarding to Postman
  Programmatic Email API. Onboarding is mostly self-service, with one exception
  listed below.
---

# Getting Started

If you’re unsure if Postman Programmatic Email API is a good fit, get started by reading the following pages:

* If you're an existing AMR user, you can check out this [comparison with AMR](comparison-with-amr.md)
* Learn more about the relevant [IM8 Policies](../overview/im8-policies.md)
* Find out how to [connect your Intranet application](../overview/connecting-your-intranet-application.md) to our API

## Ready to onboard?

{% hint style="warning" %}
**Updated 26 September 2023:** Postman will no longer be onboarding any new programmatic email API user till further notice.
{% endhint %}

Here are the following steps to take note to help you onboard more smoothly.

### **Step 1: Decide on a sender name and from address**

You can configure your from address to be either:

* The default from address: `donotreply@mail.postman.gov.sg`
* A custom from address (e.g. `noreply@agency.gov.sg`)

This decision will determine if you require our team's support to configure a custom from address. More info on this can be found [here](custom-from-address.md).

### **Step 2: Understand what content you will be sending**

To ensure that your content can be sent successfully, you should read these pages ahead of time.

* [Are you sending any attachments?](send-email-api/attachments.md)
* [Are you sending images?](send-email-api/email-body/embedding-images/)
* [Is the default send rate of 10 message/s sufficient for your use case?](send-email-api/rate-limit.md)

### **Step 3: If you want to send the emails from your own custom sender email, contact Postman team** [**here**](https://go.gov.sg/postmanp-api-wogict)

This step is optional, and only needed if you wish to set up a custom from address in [step 1](getting-started.md#step-1-decide-on-a-sender-name-and-from-email-address).

Setting up custom sender email typically takes agencies up to 2 weeks to complete so make sure you add buffer time for this step. You may refer to [this page](custom-from-address.md) for more details.

### Step 4: Generate API Key on Postman.gov.sg

Log in to Postman.gov.sg using the sender email address identified in [**Step 1**](getting-started.md#step-1-decide-on-a-sender-name-and-from-email-address) and generate the API Key. This API key will be used to authenticate your requests. You may follow the steps outlined [here](../api-key-management/generate-your-api-key.md).

{% hint style="info" %}
If you wish to use a [custom from address](custom-from-address.md), please note that the email address with which you use to log into Postman must be the same as the address from which you wish to send emails.
{% endhint %}

### **Step 5: Start sending your test emails**

Refer to the [steps here](send-email-api/) on how you can start sending your first email. Note the specific instructions on the [email body](send-email-api/email-body/), [attachments](send-email-api/attachments.md) and [email tagging and classification](send-email-api/email-tagging-and-classification.md).

As you integrate with the API:

* Find out more about the [status codes and responses you may encounter](../overview/api-response-formats.md)
* Understand [the various email statuses and error codes](tracking-email-status.md) you may encounter

### **Step 6: Communicate go-live date to Postman Team**

If you need additional support, let us know your expected go-live date. If you have reached this step independently, do give us a heads up through [this form](https://go.gov.sg/postmanp-api-wogict) before you go live.

### **Step 7: Tell us about your experience**

We always strive to improve your user experience and it would mean a lot to us if you could take a few minutes to let us know how your experience was by filling in this [form](https://go.gov.sg/postman-api-feedback).
