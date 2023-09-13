# Table of contents

* [🥳 About Postman](README.md)

## Campaign Guide - General

* [🚀 How to send a campaign?](campaign-guide/quick-start/README.md)
  * [☝ Before You Start](campaign-guide/before-you-start/README.md)
    * [Demo Mode](campaign-guide/before-you-start/demo-mode.md)

## Campaign Guide - Email

* [📧 Email Campaigns - Basics](campaign-guide/quick-start/email/README.md)
  * [How do I send an email campaign?](campaign-guide/email/how-do-i-send-an-email-campaign.md)
  * [Scheduled Sending](campaign-guide/quick-start/email/scheduled-sending.md)
  * [Bounced Emails and Halted Campaigns](campaign-guide/quick-start/email/halting-of-email-campaigns.md)
  * [Email Statistics](campaign-guide/quick-start/email/statistics.md)
  * [Formatting your Message Template](campaign-guide/quick-start/email/format-bar.md)
  * [Variable Fields](campaign-guide/quick-start/email/variable-fields.md)
  * [Unique URL Link per Recipient](campaign-guide/quick-start/email/unique-url-link-per-recipient.md)
  * [Pasting Content from Microsoft Word](campaign-guide/quick-start/email/pasting-content-from-microsoft-word.md)
  * [Manage your Unsubscriptions](campaign-guide/quick-start/email/weekly-digest-of-unsubscription.md)
  * [Understanding Unsubscriptions](campaign-guide/quick-start/email/understanding-unsubscriptions.md)
* [🔐 Sending Password-Protected Emails](campaign-guide/quick-start/password-protected-email/README.md)
  * [Tutorial](campaign-guide/quick-start/password-protected-email/tutorial.md)
  * [Template Editor](https://postman.gov.sg/test/template)

## Campaign Guide - SMS

* [📲 SMS Campaigns - Basics](campaign-guide/sms-campaigns.md)
  * [Before Starting Out](campaign-guide-sms/sms-campaigns/before-starting-out.md)
  * [Summary of Costs](campaign-guide-sms/sms-campaigns/summary-of-costs.md)
* [🪜 SMS Onboarding Overview](campaign-guide/onboarding-overview/README.md)
  * [Step 1: Sender ID Registration](campaign-guide/onboarding-overview/onboarding-step-1-senderid-registration.md)
  * [Step 2: Onboarding Form](campaign-guide/onboarding-overview/onboarding-step-2-onboarding-form.md)
  * [Step 3a: Receive Your Account Invitation](campaign-guide/sms-onboarding-overview/step-3a-receive-your-account-invitation.md)
  * [Step 3b: Set Up Your Twilio Account](campaign-guide/sms-onboarding-overview/step-3b-set-up-your-twilio-account.md)
  * [Step 4: Configure Your Twilio Account](campaign-guide/sms-onboarding-overview/step-4-configure-your-twilio-account/README.md)
    * [What if I need to buy a phone number?](campaign-guide/sms-onboarding-overview/step-4-configure-your-twilio-account/what-if-i-need-to-buy-a-phone-number.md)
  * [Step 5: Send a Test Message](campaign-guide/sms-onboarding-overview/step-5-send-a-test-message.md)
  * [Step 6: Fill in your Twilio credentials in Postman!](campaign-guide/sms/credentials.md)
    * [How do I send a campaign with my saved SMS credentials?](campaign-guide/sms/use-saved-sms-credential-in-the-campaign.md)
* [🤔 What else do I need to know about sending SMSes?](campaign-guide/sms/README.md)
  * [More about Sender ID registration](campaign-guide/sms/more-about-senderid-registration.md)
  * [Can I see the send status of my campaign?](campaign-guide/sms/sms-statistics.md)
  * [How can I configure my SMS send rate?](campaign-guide/sms/sms-send-rate.md)
  * [Sending an SMS to a Foreign Number](campaign-guide/sms/send-sms-to-a-foreign-number.md)
  * [SMS Best Practices](campaign-guide/sms/sms-best-practices.md)
  * [Useful Twilio Links](campaign-guide/sms/useful-twilio-links.md)
  * [Postman's SMS API](campaign-guide/sms/postmans-sms-api.md)

## Campaign Guide - Telegram

* [🤖 Telegram Campaigns - Basics](campaign-guide-telegram/telegram-bot/README.md)
  * [How do I set up Telegram to send my campaigns?](campaign-guide-telegram/telegram-bot/how-do-i-set-up-telegram-to-send-my-campaigns.md)
  * [Add Telegram Bot Token in Postman](campaign-guide-telegram/telegram-bot/add-telegram-bot-token-in-postman.md)
  * [Instructions for Recipient Onboarding](campaign-guide-telegram/telegram-bot/instructions-recipient-telegram.md)
  * [Use the Bot in the Campaign](campaign-guide-telegram/telegram-bot/use-the-bot-in-the-campaign.md)
  * [Telegram Formatting](campaign-guide-telegram/telegram-bot/telegram-formatting.md)
  * [Telegram Bot Statistics](campaign-guide-telegram/telegram-bot/telegram-bot-statistics.md)

## Campaign Guide - Gov.sg WhatsApp

* [📞 The official Gov.sg WhatsApp channel](campaign-guide-gov.sg-whatsapp/the-official-gov.sg-whatsapp-channel.md)

## API Guide

* [📖 Overview](api-guide/overview/README.md)
  * [IM8 Policies](api-guide/overview/im8-policies.md)
  * [Connecting your Intranet Application](api-guide/overview/connecting-your-intranet-application.md)
  * [API Response Formats](api-guide/overview/api-response-formats.md)
* [🗝 API Key Management](api-guide/api-key-management/README.md)
  * [Bearer Authentication](api-guide/api-key-management/bearer-authentication.md)
  * [Generate your API Key](api-guide/api-key-management/generate-your-api-key.md)
  * [Rotate your API Key](api-guide/api-key-management/rotate-your-api-key.md)
* [📨 Programmatic Email API](api-guide/programmatic-email-api/README.md)
  * [Getting Started](api-guide/programmatic-email-api/getting-started.md)
  * [Comparison with AMR](api-guide/programmatic-email-api/comparison-with-amr.md)
  * [SG-Mail Whitelisting](api-guide/programmatic-email-api/sg-mail-whitelisting.md)
  * [Custom From Address](api-guide/programmatic-email-api/custom-from-address.md)
  * [Tracking Email Status](api-guide/programmatic-email-api/tracking-email-status.md)
  * [Send Email API](api-guide/programmatic-email-api/send-email-api/README.md)
    * [From Name and From Address](api-guide/programmatic-email-api/send-email-api/from-name-and-from-address.md)
    * [CC and BCC](api-guide/programmatic-email-api/send-email-api/cc-and-bcc.md)
    * [Recipient Blacklist](api-guide/programmatic-email-api/send-email-api/recipient-blacklist.md)
    * [Email Tagging and Classification](api-guide/programmatic-email-api/send-email-api/email-tagging-and-classification.md)
    * [Email Body](api-guide/programmatic-email-api/send-email-api/email-body/README.md)
      * [Embedding Images](api-guide/programmatic-email-api/send-email-api/email-body/embedding-images/README.md)
        * [Linked Images](api-guide/programmatic-email-api/send-email-api/email-body/embedding-images/linked-images.md)
        * [Content-ID Images](api-guide/programmatic-email-api/send-email-api/email-body/embedding-images/content-id-images.md)
    * [Attachments](api-guide/programmatic-email-api/send-email-api/attachments.md)
    * [Rate Limit](api-guide/programmatic-email-api/send-email-api/rate-limit.md)
  * [Get Email by ID API](api-guide/programmatic-email-api/get-email-by-id-api.md)
  * [List Emails API](api-guide/programmatic-email-api/list-emails-api.md)
* [📨 Programmatic GovSG WhatsApp API](api-guide/programmatic-govsg-api/README.md)
  * [Getting Started](api-guide/programmatic-govsg-api/getting-started.md)
  * [Tracking Message Status](api-guide/programmatic-govsg-api/tracking-message-status.md)
  * [Get Available Templates API](api-guide/programmatic-govsg-api/get-templates-api.md)
  * [Send Message API](api-guide/programmatic-govsg-api/send-message-api.md)
  * [Get Message by ID API](api-guide/programmatic-govsg-api/get-message-by-id-api.md)
  * [List Messages API](api-guide/programmatic-govsg-api/list-messages-api.md)
* [🤳 Programmatic SMS API](api-guide/programmatic-sms-api.md)
* [🎓 Frequently Asked Questions](api-guide/frequently-asked-questions.md)

## FAQ

* [Postman Uptime](faq/postman-uptime.md)
* [For Recipients](faq/faq-recipients/README.md)
  * [Check Email Authenticity](faq/faq-recipients/check-email-authenticity.md)
* [For Senders](faq/faq-sender/README.md)
  * [Messaging Channel Comparison](faq/faq-sender/messaging-channel-comparison.md)
  * [Cost Breakdown](faq/faq-sender/cost-breakdown.md)

## Legal

* [Terms & Conditions](legal/t-and-c.md)
* [Privacy Policy](legal/privacy.md)

***

* [Contact Us](contact-us.md)
* [GitHub](https://github.com/opengovsg/postmangovsg/)
