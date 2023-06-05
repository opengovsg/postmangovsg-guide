---
description: >-
  This page gives you an overview of what to expect when onboarding to Postman
  Programmatic API. Onboarding is completely self-service, with one exception
  listed below.
---

# Get Started

If you’re not sure what Postman API is but is keen to explore Postman, make sure that you have noted the following before proceeding:

* [Comparison with AMR](comparison-with-amr.md): to assess whether Postman API fits your use case
* [IM8 Policies](../overview/im8-policies.md): to make sure that your system can connect to Postman API
* [Connecting your intranet application](../overview/connecting-your-intranet-application.md): to make sure that you understand if your systems is suitable to be using our Programmatic API.
* If your system is sending emails via SMTP, do let us know through [this form](https://go.gov.sg/postmanp-api-wogict).

If you still have questions, you may reach out to us through [this form](https://go.gov.sg/postmanp-api-wogict).

## Ready to onboard?&#x20;

Here are the following steps to take note to help you onboard more smoothly.&#x20;

### **Step 1: Decide on a sender name and from email address**

This step is important as it will determine if you require our team's support to configure your custom from email sender address.&#x20;

There are two configuration of your sender email address:

* Default sender email will be [**donotreply@mail.postman.gov.sg**](mailto:donotreply@mail.postman.gov.sg)
* Specify any **custom from email sender** **(e.g** [**noreply@agenc.gov.sg**](mailto:noreply@agenc.gov.sg)**)** if you prefer to send the emails from your own domain.

More on this can be found [here](custom-from-address.md).&#x20;

### **Step 2: Understand what content you will be sending**

To ensure that your content can be sent successfully, you should read these pages ahead of time.&#x20;

* [Are you sending any attachments?](send-email-api/attachments.md)
* [Are you sending images?](send-email-api/email-body/embedding-images/)
* [Is the send rate 10 message/s sufficient for your use case?](send-email-api/rate-limit.md)

### **Step 3: If you want to send the emails from your own custom sender email, contact Postman team** [**here**](https://go.gov.sg/postmanp-api-wogict)**.**

This step is optional, and only needed if you chose to send from your own email domain in [step 1](get-started.md#step-1-decide-on-a-sender-name-and-from-email-address).

Setting up custom sender email typically takes agencies up to 2 weeks to complete so make sure you buffer in time for this process. You may refer to [this page](custom-from-address.md) for more details.

### **Step 4: Generate API Key on** [**Postman.gov.sg**](http://postman.gov.sg)

Log in to [Postman.gov.sg](http://postman.gov.sg) using the sender email address identified in [**Step 1**](get-started.md#step-1-decide-on-a-sender-name-and-from-email-address) and generate the API Key. This API key will be used to authenticate your requests. You may follow the steps outlined here.

{% hint style="warning" %}
The API key should be generated from the email account that you will be sending the emails from
{% endhint %}

### **Step 5: Start sending your test emails**

Refer to the [steps here](send-email-api/) on how you can start sending your first email. Note the specific instructions on the [email body](send-email-api/email-body/), [attachments](send-email-api/attachments.md) and [tagging](send-email-api/email-tagging-and-classification.md).

As you are testing the API, there are a few key things to take note:

* [List of API response formats to help you understands the success or error codes you see](../overview/api-response-formats.md)
* [Tracking the status](tracking-email-status.md) of the emails and error you encounter to understand is the error you receive.

### **Step 6: Communicate go live date with Postman Team**

Make sure that you have communicated to the Postman team in advance on your expected go live date, we will ensure that the team is around to render any support you may require. If you have reached this step independently, do give us a heads up through [this form](https://go.gov.sg/postmanp-api-wogict) before you go live.&#x20;

### **Step 7: Tell us how your experience was**

We always strive to improve your user experience and it would mean a lot to us if you could take a few minutes to let us know how your experience was by filling in this [form](https://go.gov.sg/postman-api-feedback).&#x20;



