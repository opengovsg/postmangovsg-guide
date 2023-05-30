---
description: >-
  Phone number purchase is necessary if you are sending SMSes to foreign
  numbers. Follow the steps here to purchase a number.
---

# What if I need to buy a phone number?

#### This step must be done before setting up your messaging service ID.

### How to buy a phone number?

On the left console, select `Develop > Phone Numbers > Manage > Buy a number.`

<figure><img src="../../../.gitbook/assets/image (5).png" alt="" width="230"><figcaption><p>Buy your number</p></figcaption></figure>

Select the phone number that you prefer.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Buy your number</p></figcaption></figure>

### How to set up messaging service ID with phone number?

You need to create a messaging service and tie the phone number that you bought to this messaging service before you can send SMSes.&#x20;

Go back to your Twilio home page, and select`Set up a Messaging Service`.

<figure><img src="../../../.gitbook/assets/image (23).png" alt=""><figcaption><p>Set up your messaging service</p></figcaption></figure>

On the side bar, click `Develop > Messaging > Services > Create Messaging Service.`

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption><p>Create your messaging service</p></figcaption></figure>

Name your messaging service and indicate the purpose. This will help you better identify your use cases if you have multiple, and will also help Twilio detect your specific use case quicker should you need their help for troubleshooting.

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption><p>Set it up</p></figcaption></figure>

Add your `Sender Pool`. Sender Pool is where you configure the sender details such as the phone number you bought, and input your alphanumeric SenderID.

Click `Add Senders.`

<figure><img src="../../../.gitbook/assets/image (22).png" alt=""><figcaption><p>Set up sender pool</p></figcaption></figure>

Add the phone number you purchased to this service.

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Select "Phone Number"</p></figcaption></figure>

Select the number you want to associate with this messaging service (if you have more than one).

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Select desired number</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Number selected successfully</p></figcaption></figure>

Then, go back [here](https://guide.postman.gov.sg/campaign-guide/onboarding-overview/step-4-configure-your-twilio-account#set-up-your-alphanumeric-senderid) to continue the set-up of your alphanumeric senderID.
