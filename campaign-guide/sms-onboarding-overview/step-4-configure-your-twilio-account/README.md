---
description: >-
  Now that the administrative set-up is done, you can set up your Twilio
  credentials! Follow the steps here in chronological order. This is a one-time
  set-up.
---

# Step 4: Configure Your Twilio Account

### Before you start, note the credentials you'll need to save-keep to input into Postman:

1. account SID
2. API key SID
3. your secret key (_this is unretrievable once you proceed beyond this step, so make sure you have saved somewhere, or you will need to redo the set-up process to generate new keys_).
4. messaging service ID&#x20;

### 1. Your Account SID

An account SID is the unique identifier assigned to your agency account, much like an NRIC number. This is immediately available on your dashboard once you log into your account console.

<figure><img src="../../../.gitbook/assets/image (23).png" alt=""><figcaption><p>Locate your account SID</p></figcaption></figure>

### 2. Your API key SID

To set up your API key for Postman, select **`API keys & tokens`** on the side dashboard under **Accounts**.

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption><p>Select "API keys &#x26; tokens"</p></figcaption></figure>

Then, create a new **standard** API key by selecting `Create API key`.

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption><p>Select "Create API key"</p></figcaption></figure>

Create a `friendly name` for your API key so you can easily identify it in the future, and select `Standard` as the API key type.

<figure><img src="../../../.gitbook/assets/image (15).png" alt=""><figcaption><p>Name your API key, and set key type as "standard"</p></figcaption></figure>

### 3. Your Secret Key

Save your `secret key` - <mark style="color:red;">**remember, once you lose this or if you do not save it, you will NOT be able to retrieve it again after moving on to the next step!**</mark>&#x20;

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption><p>Save the API key SID and Secret Key somewhere safe!</p></figcaption></figure>

<mark style="color:red;">Make sure you copy and save these details somewhere safe.</mark> Then, check the box and click "DONE".

### 4. Your messaging service SID (without buying a phone number)

This is the last detail you need to save before proceeding to Postman.

{% hint style="info" %}
Note: we used to ask users to purchase a US phone number at USD$1.15. This will enable a one-way messaging ability (from you to recipient). With the implementation of the senderID regime by IMDA, this is no longer required - _only if you are sending ONLY to Singapore numbers._

**However, if you are sending SMSes to foreign numbers,** you will still need to purchase a phone number. Otherwise, your messages will not be delivered. Find out how to purchase a phone number [here](what-if-i-need-to-buy-a-phone-number.md), and follow these [steps](what-if-i-need-to-buy-a-phone-number.md) to set up your messaging service ID. You can ignore the steps below if you are purchasing a phone number.


{% endhint %}

**If you don't have a need to purchase a phone number, follow these steps to obtain your messaging service SID.**

Go back to your Twilio home page, and select`Set up a Messaging Service`.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Click "Set up a Messaging Service"</p></figcaption></figure>

On the side bar, click `Develop > Messaging > Services > Create Messaging Service.`

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption><p>Create your messaging service</p></figcaption></figure>

Name your messaging service and indicate the purpose. This will help you better identify your use cases if you have multiple, and will also help Twilio detect your specific use case quicker should you need their help for troubleshooting.

<figure><img src="../../../.gitbook/assets/image (17).png" alt=""><figcaption><p>Fill in the required details</p></figcaption></figure>

#### Set up your alphanumeric senderID

Configure your alphanumeric senderID by selecting `Alpha Sender` under `Add Senders > Sender Type.`

<figure><img src="../../../.gitbook/assets/image (20).png" alt=""><figcaption><p>Select "Alpha Sender"</p></figcaption></figure>

Click Continue. _You may ignore the notification indicating that Alphanumeric Sender is not enabled for this account._

<mark style="color:red;">**Specify the Alphanumeric Sender ID you want to use in the text box. It is best to align this with the SenderID that you registered with SGNIC.**</mark>

<figure><img src="../../../.gitbook/assets/image (31).png" alt=""><figcaption><p>Add in your SenderID</p></figcaption></figure>

**If the Alphanumeric Sender ID you chose is protected,** you will notice either of the two things below.

* You encounter an error when setting it up on the Sender Pool page
* You may not receive any message when you send a test SMS

This also means that this Sender ID has been registered by another entity and you will not be able to use it.

Once you have completed the step above, you may click the `Skip Setup` button below.

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Complete the set up</p></figcaption></figure>

After clicking "Skip setup" in the step above, you should be brought to the Properties page of this Messaging Service. On this page, you should be able to find the **Messaging Service ID**.

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption><p>This is your messaging service SID</p></figcaption></figure>
