---
description: >-
  Please read through this guide to understand the difference between hard and
  soft bounces, as well as halted campaigns.
---

# Bounced Emails and Halted Campaigns

## What are the different kinds of bounce?

Emails like abc@gmail.com may look like a well-formatted email address, but if it is not managed by a real human being, services like Google will send a bounce message when the email is sent out. This is considered a hard bounce, which increases Postman's bounce rate and negatively affects Postman's reputation score.

1. **Hard bounce:** Invalid email addresses.
2. **Soft bounce:** Out-of-office messages or message notifications that the recipient's email inbox is full.

## What is the impact of a hard bounce?

Hard bounce affects Postman's reputation score. A reputation score is a measure of the email service reputation. **Postman needs to maintain a low bounce rate in order to have a good reputation score.** Think of this as having good credit from the bank. Banks need you to have a good credit score in order to provide a credit card for transactions. Similarly, Postman needs a good reputation score to send emails to Internet Service Providers (ISPs) in order to deliver emails to recipients.

## What do you need to do as a user to help Postman retain a good reputation score?

We need your help as a user to ensure that your mailing list is clean before you send an email campaign through our service. We understand that the first email campaign that you send out might contain a lot of invalid email addresses, but we ask you to use the bounce list once your campaign is over to clean and maintain your contact list.

## Why is my campaign halted?

A campaign will be halted when there are too many hard bounces (due to invalid email addresses, which are addresses that do not exist), and will affect Postman's reputation score.

Postman encourages all users to maintain clean contact lists as a best practice, which means that email addresses should be valid and subscribed to the mailing list.

To ensure that your campaign will not be halted, especially campaigns of high time sensitivity and urgency, please check that your mailing lists are clean before uploading them in CSV format to your Postman campaign:

1. check with your source system to ensure that no invalid addresses are included in the list e.g. non-existent email addresses, misspelled email addresses.
2. unsubscribe requests are adhered to - it is also good practice to remove unsubscribers when the request is received, though discretion of doing so is left to the agency in case of critical content.

If your halted campaign has high time sensitivity or high urgency (e.g. impact on MoP is high/ops will be severely impaired if campaign is not immediately sent out), please [contact us](https://form.gov.sg/#!/62b19812ff209e00126f2c47) for assistance.

## What are some ways to ensure my contact list is clean?

Here are some tips in building and maintaining your mailing list:

1. **Ensuring verified email collection upstream**: Consider using FormSG’s `verified email field` to collect email addresses from the intended recipients. This will ensure that you only collect email addresses from people who have access to the email account.
2. **Remove invalid email addresses from your mailing list**: We know that email addresses can become invalid over time when recipients change email addresses. You should always clean your mailing list regularly. You can do this easily with our export button on the campaign dashboard page. If an email campaign has bounced emails (hard bounce), it will be captured in the .csv file.
3. **Check for formatting errors:** Make sure that the format for the email is correct, e.g. recipient@example.com. You can use this [tool](https://observablehq.com/@jeantanzj/email-validation) to do a quick check for any major formatting problems.

{% hint style="warning" %}
Do not collect emails through Zoom registration forms. We know from experience that people do not put in their real emails in these forms.
{% endhint %}

## Suspect that your list might need cleaning up?

{% hint style="info" %}
If your lists are from some time ago, or you know that it hasn't been maintained in some time, we would advise you to use this [Bulk Email Checker](https://bulk.email-checker.net/) to clean your list before uploading it in Postman. This helps you ensure that your campaigns will not be halted, especially if they are urgent campaigns.
{% endhint %}
