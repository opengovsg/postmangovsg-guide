# Recipient Blacklist

## Purpose

We keep a blacklist of email addresses to whom our system will not send emails. Typically, these email addresses are added to the blacklist after a delivery attempt has resulted in a hard bounce, (e.g. the email address does not exist).

Without a blacklist, our system would continue to attempt to send emails to these addresses, which would result in a poor reputation for our system and adversely impact the deliverability of emails to other recipients.

For more information on email deliverability, you can visit [AWS SES's documentation](https://docs.aws.amazon.com/ses/latest/dg/send-email-concepts-deliverability.html).

## Is my recipient on the blacklist?

Currently, we do not provide a way to check if a recipient is on the blacklist prior to sending out an email.

However, there are two ways you will be informed if a recipient is on the blacklist:

1. In our current setup, during your API call to our system, we will check if the recipient is on the blacklist. If the recipient is on the blacklist, we will return an error message indicating that the recipient is on the blacklist. However, to scale our system, we plan to change this behavior in the future, so we advise against relying on this behavior.
2. You can query an email by its ID using this [API endpoint](../get-email-by-id-api.md). If the email was not sent because the recipient was on the blacklist, this will be indicated in the `errorCode` field of the response.

## How do I remove a recipient from the blacklist?

There are some instances where a blacklisted recipient may be a valid recipient. For example, if a recipient's email address was blacklisted because it did not exist, but the recipient has since created an email address with the same email address, then the recipient should be removed from the blacklist.

In this case, you should [contact us](https://go.gov.sg/postman-contact-us) to remove the recipient from the blacklist.
