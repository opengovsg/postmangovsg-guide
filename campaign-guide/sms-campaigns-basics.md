---
description: >-
  Send mass SMSes with Postman! These SMSes are sent through Twilio, our SMS
  aggregator. We will guide you through setting up an account with Twilio,
  before you can begin sending SMSes on Postman.
---

# 📲 SMS Campaigns - Basics

### What is the difference between Twilio and Postman?

Postman is a free multi-channel communications platform built by Open Government Products for all public service agencies. Postman provides a convenient interface for you to craft your message, upload your recipient list, and send your campaign. Using Postman itself is free.

Twilio is a commercial cloud communication service that allows users to send messages (including SMS) through an Application Program Interface (API). Twilio bills users directly for its services; in this case, any SMSes you send using the Postman interface will be billed to you directly by Twilio. Postman does not pay for the SMSes that you send, but neither does Postman charge you for sending SMSes using our interface.

### Why Twilio?

We evaluated other cloud-based SMS service providers like Nexmo and AWS SNS before we chose Twilio. We chose Twilio for its simple user interface with an interactive debugger. Its API documentation is also well written, and its API easy to set up. The API also optimises the rate limit to send bulk messages, and allow for users to retry for messages with errors during the first attempted delivery.&#x20;

Importantly, Twilio API's success rate is 99.999% & uptime is around 99.95% monthly.&#x20;

Since inception, we have used Twilio for SMS sending services, such as NDP ticketing, Digital MCs, SGH's elective surgery appointment reminders, and quarantine ops by MOH and ICA during Covid-19.

### Can I trial using Postman to send SMSes before deciding whether to onboard onto Twilio?

We understand that setting up your Twilio account to obtain the credentials to input in Postman, as well as settling billing processes, may take time. Therefore, we offer all user accounts **3** free demo SMS campaigns per account, at up to **20** free SMSes per campaign, so that you can try out the Postman interface for yourself. No need to set up Twilio credentials at this point. Simply log in with your gov.sg email address and click on `Create a demo campaign now`. If it's your first time logging into Postman, click `Try demo SMS/Telegram`.

<figure><img src="../.gitbook/assets/Screenshot 2023-05-30 at 3.29.44 PM.png" alt=""><figcaption><p>For new Postman users</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2023-05-30 at 3.28.37 PM (1).png" alt=""><figcaption><p>Dashboard view for Postman users with existing campaigns</p></figcaption></figure>

### I've decided to use Postman to send my SMS campaigns! What do I need to do now?

We're happy to hear that you want to onboard! Click over to the next page for more instructions on how to get started. Broadly, these are the steps you need to take:

1. Register your desired SenderID with SGNIC
2. Fill in our SMS WOG Onboarding Form.
3. Accept your Twilio account invitation and proceed to set up your account.
4. Fill in your Twilio credentials in Postman. This is a one-time set-up.
5. Start using Postman to send your SMSes!
