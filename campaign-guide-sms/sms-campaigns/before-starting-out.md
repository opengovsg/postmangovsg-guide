---
description: What else do I need to know about Twilio/Postman, before I commit?
---

# Before Starting Out

### Useful Information

* [**Send rate**](https://support.twilio.com/hc/en-us/articles/115002943027-Understanding-Twilio-Rate-Limits-and-Message-Queues)**:** SMSes are sent by Twilio at a default of 10 messages per second. If you would like to increase this rate, you will need to liaise with Twilio to configure this, and then configure it in your Postman dashboard. More on how to do so [here](../../campaign-guide/sms/sms-send-rate.md).
* **SMS character** [**limit**](https://www.twilio.com/docs/glossary/what-sms-character-limit)**:** each message segment is capped at 160 characters. Beyond this character limit, the single SMS will consist of 2 or more message segments, depending on the length of your SMS. You will be charged at a per-message-segment rate.
* **Resources**: each agency/department will need its own Twilio account set up before SMSes can be sent via Postman. This is for billing and governance purposes. Not to worry - we will guide you through the set up of this account!
* **Maximum number of SMSes:** there is no limit to how many SMSes or recipients you can send using Postman's interface. Our record is 144,000 SMSes sent in 1 batch by a government agency.
* **1-way SMS:** currently, sending SMSes on Postman is one-way only. What this means is that agencies can send mass SMSes to recipients using Postman, but there is currently no functionality on Postman for you to receive any responses that your recipients might send.

### Billing and Costs

Twilio works on a pre-payment method - you will need to top up your account with credits before SMSes can be sent. [Recharge triggers](https://support.twilio.com/hc/en-us/articles/223135607-How-do-I-set-a-recharge-or-notification-trigger-) can be set so that you don't have to manually top up these credits.

Billing is generally done using a _corporate credit card._ Read more about Twilio's billing methods [here](https://support.twilio.com/hc/en-us/articles/360042138913-Payment-Options-for-Twilio-Invoices).

{% hint style="info" %}
If you are unable to obtain a corporate credit card, you can explore direct invoicing with Twilio. However, Twilio requires a minimum spend of US12,000 annual (or about 25,000 SMSes per month) to qualify for this mode of payment.
{% endhint %}

#### What is the cost?

At this point of writing (May 2023), it costs USD$0.0415 per message segment of 160 characters to send to recipients with Singapore numbers. If your message is longer than 160 characters, you will be charged the cost of as many message segments.

You may refer to Twilio's [page](https://www.twilio.com/sms/pricing/sg) for the latest rates. You will be charged the cost according to the destination handset i.e. you will be charged the US rate for sending to a US number, even if the recipient with this number is based in Singapore.
