# CC and BCC

Our email API supports CC and BCC.

## What is CC and BCC?

CC stands for "Carbon Copy" and BCC stands for "Blind Carbon Copy." Both are features in an email system that allow you to send the same message to multiple recipients.

1. **CC**: When you CC someone on an email, the CC list includes recipients who should receive a copy of the email for their information. Everyone included in the To and CC fields can see who else received the email, including the email addresses of other recipients listed in the CC field. It's often used when the information contained in the email is relevant to the individuals in the CC field, but they're not the primary recipients who need to take action.
2. **BCC**: The BCC feature works similarly to CC in terms of sending the email to multiple recipients. However, when you add recipients to the BCC field, those email addresses are hidden from all other recipients. Even other BCC recipients cannot see each other's email addresses. This is a useful feature when you want to protect the privacy of certain recipients, or you want to communicate without revealing to the main recipients that you're also communicating with others.

## How It Works

You can add CC and BCC recipients to your email by adding the `cc` and `bcc` fields to your API request. The `cc` and `bcc` fields each accept an array of email addresses.

An example JSON payload making use of the `cc` and `bcc` fields:

```JSON
{
  "recipient": "primary-recipient@email.com",
  "subject": "subject",
  "body": "body",
  "cc": ["cc-recipient@email.com"],
  "bcc": ["bcc-recipient@email.com"]
}
```

## Limitations

1. Due to our underlying email provider, each email can have a maximum of 50 recipients (including the primary recipient, CC recipients, and BCC recipients). Note that our API is designed to only allow one primary recipient per email.
2. If the primary recipient is on our blacklist, the email won't be sent. If there are blacklisted recipients in the `cc` or `bcc` fields, these recipients will be ignored and the email will still be sent to the other recipients.
3. Within each array of `cc` and `bcc` recipients, no duplicate email addresses are allowed.
4. The [email status](../tracking-email-status.md#email-status) of CC and BCC recipients are not tracked.
5. The email status of the primary recipient is still tracked, but the `OPEN` status of an email with CC and BCC email is not accurate as [the tracking pixel](../tracking-email-status.md#tracking-open-rates) will be triggered when any of the recipients open the email. This is an inherent limitation of the tracking pixel as the content of the email is identical for all recipients.
