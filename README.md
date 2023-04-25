# What is PostmanSG

PostmanSG is a mass messaging tool for the Singapore Government.

We've since sent out more than 100 million messages from over 90 agencies. This includes quarantine orders, COVID-19 test results and employer notices.

Start using PostmanSG by logging in with an `@agency.gov.sg` email address!

## What can PostmanSG do?

* **Easily customize messages to reach a wide audience**: Create a message template, upload a file containing customization parameters, and we will handle the rest for you.
* **Mass send emails**: Just click `Send campaign` and PostmanSG will send those messages out to your intended audience via email.
* **Mass send SMSes**: Enter your Twilio credentials under `Settings`, and PostmanSG will send those messages via SMS. No integration with Twilio is needed.
* **Mass send Telegram messages through a bot**: Get your recipients to subscribe to your Telegram bot and use PostmanSG to send Telegram messages to the subscribers by uploading the subscriber's contact list.
* **View stats**: Keep track of your campaign's progress as it is sending and check back when it is completed.
* **Scheduled sending**: Create your campaign but send it out at a later **time**.

## Is PostmanSG secure?

Email and SMS are not 100% secure. We recommend against putting any sensitive information in the email or SMS content. To transmit sensitive content, some users generate a recipient-specific unique link to a locked page. We have completed our VAPT on June 15th, 2020.

## Can PostmanSG be accessed on the government intranet?

PostmanSG is only available on the internet at the moment.

## What data can PostmanSG handle?

We use cloud infrastructure so we can handle up to **Confidential (Cloud-Eligible)** data. When in doubt, you should follow IM8’s guidelines on data classification.

| Normal email/SMS/Telegram | Non-sensitive to sensitivity low-normal | <ul><li>Transaction</li><li>Notification</li><li>Information broadcast</li><li>Receipts</li><li>Reminders</li></ul> |
| ------------------------- | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Password-protected email  | Sensitivity high/restricted             | <ul><li>COVID-19 test result</li><li>Blood test result</li><li>Exam test result</li></ul>                           |

## Difference between the Web App and Programmatic APIs

**Web App:** Users can access PostmanSG by going to [https://postman.gov.sg](https://postman.gov.sg). The web app is a user interface that allows all users to send campaigns.

**Programmatic APIs**: In addition to campaigns, we also allow technical users to call our APIs to send messages programmatically. This typically requires a system integration involving your engineers or IT support. In order to use this feature, you need to generate an API key from `Settings` in the PostmanSG web app. You can find more by going to our API Guide [here](https://guide.postman.gov.sg/api-guide/overview).

| Access Type                                                                                        | Channels                     | Type of Use Case             | Prerequisite                                                                                                                                                                                              |
| -------------------------------------------------------------------------------------------------- | ---------------------------- | ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [API](https://github.com/opengovsg/postmangovsg/blob/master/docs/api-usage.md)                     | Email & SMS                  | System-generated             | Engineering or IT team to send messaging info from the source system to PostmanSG.                                                                                                                          |
| [Web app](https://guide.postman.gov.sg/guide/getting-started) | Email, SMS, and Telegram Bot | Manual intervention required | <p>`@agency.gov.sg` email access to log in</p><p><br>Fill out an access request <a href="https://go.gov.sg/postman-non-gov-sg-application">form</a> if you do not have an `@agency.gov.sg` email address.</p> |

## Open-source contribution

PostmanSG is open-sourced. Visit our [GitHub repo](https://github.com/opengovsg/postmangovsg) to start contributing to our code. Contributing guidelines can be found [here](https://github.com/opengovsg/postmangovsg/blob/master/docs/CONTRIBUTING.md).

![](.gitbook/assets/github-icon-png-26.jpg)
