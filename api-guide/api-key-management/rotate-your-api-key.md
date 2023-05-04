# Rotate your API Key

## Multi API Key Support <a href="#new-multi-api-key-support" id="new-multi-api-key-support"></a>

If multiple teams in your agency is sharing the same email account (e.g \[email protected]), you can now create multiple API keys on Postman for multiple teams.

Simply navigate to Settings and generate another API key.

![](https://1981680851-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MAQH3DF49Lq0AJudrbF%2Fuploads%2F48ILTLC0pBxHPfowA0mb%2FScreenshot%202023-04-06%20at%209.00.28%20AM.png?alt=media\&token=84ea4a1c-951b-4c9e-af36-79bed43e0dbd)

## API Key Expiry and Rotation <a href="#coming-soon-api-key-expiry" id="coming-soon-api-key-expiry"></a>

Since API keys need to be stored, passed around, and leveraged in the development of solutions that interact with our Postman system, there are opportunities for these API keys to be compromised. API keys should be rotated to ensure that data cannot be accessed with an old key that might have been lost, cracked, or stolen. Rotating API keys will reduce the window of opportunity for an access key that is associated with a compromised or terminated account to be used.

At Postman, we have a hard-limit of 6 months for API key expiration, which means that any API keys that have been created more than 6 months from the current date is not usable anymore. We encourage users to rotate API keys even more frequently if you can afford to.

### How to rotate an API key

In the event you have found that your current API key has been leaked, or your current API Key is expiring soon, follow these steps to rotate your API Key:

* Create a new API Key on the dashboard and save the value locally in your computer's note.
* Update the API key used in your system to the new one and restart your system to load the new value if needed.
* Remove the old API key from your account by clicking the delete button in the table in settings page. Please ensure that you are deleting the correct API key.

**Note:** Make sure that the above steps are followed in chronological order that they're written in, otherwise your system might not be able to request to Postman for the update time period

### Notification Schedule

Before your API key expires, we will attempt to get in touch with you using the contact emails provided as part of the information about a particular API key of yours according to the below schedule:

* 1 month before the expiry date
* 2 weeks before the expiry date
* 3 days before the expiry date
* 1 day before the expiry date
