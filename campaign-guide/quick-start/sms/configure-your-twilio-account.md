---
description: Follow step by step for a successful set-up.
---

# Configure your Twilio Account

Information you will need to keep at the end of the set-up, to key into your Postman dashboard:

* account SID
* API key SID
* secret key
* messaging service ID

Your **account SID** is on the dashboard when you log in to your agency's account console. This is the unique identifier assigned to your agency account, much like an NRIC number.

<figure><img src="../../../.gitbook/assets/Screenshot 2023-01-27 at 11.24.55 PM.png" alt=""><figcaption></figcaption></figure>

## Step 1: Set up technical details

### a) Set up a Standard API Key

To set up your API key for Postman, select **`API keys & tokens`** on the side dashboard under **Accounts**.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-11-02 at 4.03.20 PM.png" alt=""><figcaption></figcaption></figure>

Then, create a new **standard** API key by selecting `Create API key`.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-10-31 at 5.18.22 PM.png" alt=""><figcaption></figcaption></figure>

Create a `friendly name` for your API key so you can easily identify it in the future, and select `Standard` as the API key type.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-10-31 at 5.20.52 PM (1).png" alt=""><figcaption></figcaption></figure>

We need your `Account SID` and `secret key` for Postman. Please keep these safe.

<mark style="color:red;">**Remember to save the secret key somewhere, as you will not be able to retrieve it again after moving on to the next step**</mark>**.**

Once you have it stored somewhere safe, check the box and click “Done”.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-10-31 at 5.21.51 PM.png" alt=""><figcaption></figcaption></figure>

### b) Buy a phone number

{% hint style="info" %}
**You need to purchase a phone number to start using Postman.** If you are using a trial account on Twilio and did not put a corporate credit card on file then this is as far as you can go.
{% endhint %}

A Singapore phone number is USD$80 per month. We recommend that you buy a US phone number which is USD$1.15 per month. Aside from cost savings, the US phone number is sufficient for Postman's current capabilities in sending 1-way messages (from you to recipient).

If you have use cases for 2-way SMS (in which case a Singapore number will be necessary), please reach out to us [here](http://localhost:5000/s/-MAQH3DF49Lq0AJudrbF/).

{% hint style="info" %}
With the implementation of [mandatory registration](https://sgnic.sg/smsregistry/overview) of SenderIDs by SGNIC, it is possible for SMSes to be sent through Twilio without a phone number. However, these SMSes will only be able to reach recipients with Singapore phone numbers. SMSes will not be delivered to foreign phone numbers.
{% endhint %}

### How to buy a phone number?

On the left console, select Develop > Phone Numbers > Manage > Buy a number.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-10-31 at 5.33.00 PM.png" alt=""><figcaption></figcaption></figure>

Then select the phone number that you prefer.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-10-31 at 5.34.33 PM.png" alt=""><figcaption></figcaption></figure>

## c) Set up your messaging service on Twilio

You need to create a messaging service and tie the phone number that you bought to this messaging service before you can send SMSes.

#### Create a new messaging service

Go back to your Twilio home page, and select`Set up a Messaging Service`.

<figure><img src="../../../.gitbook/assets/Screenshot 2022-11-02 at 3.41.46 PM.png" alt=""><figcaption></figcaption></figure>

On the side bar, click `Develop > Messaging > Services > Create Messaging Service.`

<figure><img src="../../../.gitbook/assets/Screenshot 2022-11-02 at 3.46.58 PM.png" alt=""><figcaption></figcaption></figure>

Name your messaging service and indicate the purpose. This will help you better identify your use cases if you have multiple, and will also help Twilio detect your specific use case quicker should you need their help for troubleshooting.

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.03.37 PM.png>)

#### Add Sender Pool

Sender Pool is where you configure the sender details such as the phone number you bought, and input your alphanumeric SenderID.

Click `Add Senders`

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.03.51 PM.png>)

Add the phone number you purchased to this service.

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.04.02 PM.png>)

Select the number you want to associate with this messaging service (if you have more than one).

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.05.52 PM (1).png>)

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.06.05 PM (1).png>)

### d) Configure Alphanumeric SenderID on Twilio

The steps below are in addition to registering your SenderID with SGNIC. Both steps are necessary to complete the set up process.

#### On your Twilio console

Click on Add Senders and select Alpha Sender. This must be done after you configure the phone number setup in [Step 4](configure-your-twilio-account.md#step-4.-set-up-your-messaging-service).

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.06.21 PM.png>)

Click Continue. _You may ignore the notification indicating that Alphanumeric Sender is not enabled for this account._

**Specify the Alphanumeric Sender ID you want to use in the text box. It is best to align this with the SenderID that you registered with SGNIC.**

![Configure your Alphanumeric Sender ID](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.07.11 PM.png>)

**If the Alphanumeric Sender ID you chose is protected,** you will notice either of the two things below.

* You encounter an error when setting it up on the Sender Pool page
* You may not receive any message when you send a test SMS

This also means that this Sender ID has been registered by another entity and you will not be able to use it.

Once you have completed the step above, you may Click the Skip Setup Button below.

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.07.36 PM.png>)

## Step 2: Get your Messaging Service ID

After clicking "Skip setup" in the step above, you should be brought to the Properties page of this Messaging Service.

### Copy Messaging Service ID

On this page, you should be able to find the **Messaging Service ID** that we require you to key into Postman.

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.09.17 PM.png>)

## Step 3: Name your account

This step helps us and Twilio better identify your account should you need help, without having to go into your account itself, which we prefer in order to respect the privacy and security of your account.

Go to `Account > General settings > Account details > Account name`

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

And **rename your account with the format `Agency-Department name-Use case`**

## Step 11: Send a test message to yourself

Navigate back to the console and under **Try it out**, select **Send an SMS.** Insert your own phone number and select the messaging service that you've just setup earlier in [Step 4](configure-your-twilio-account.md#step-4.-set-up-your-messaging-service).

Type your message and click send to check if you receive the SMS and if the SenderID is accurate.

![](<../../../.gitbook/assets/Screenshot 2022-06-07 at 10.52.40 PM (1).png>)

**If you don't receive your test SMS**, it is likely that this SenderID has been taken by another agency. You should use another Alphanumeric Sender ID. Otherwise, you may reach out to Twilio's support team for help.

Once you've setup your Twilio Account, you should insert the required [fields](credentials.md) into PostmanSG and you can start sending out SMS through PostmanSG using this Twilio credential.

You should not need to configure your Twilio account in the future.

{% hint style="danger" %}
**Do not release your number**: Releasing a number means that you are returning the number you have purchased back to Twilio. This is irreversible. They will charge you for a new number when you make a future purchase.
{% endhint %}