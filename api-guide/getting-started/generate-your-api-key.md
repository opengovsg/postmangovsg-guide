# Generate your API Key

Before you start using our API, you have to generate an API key. This API key can be used to make API calls and serve to authenticate you to our system. Keep this API key safe and do not share it with anyone.

All users that can log into `postman.gov.sg` are able to generate this API key and use it call Postman API.

## Bearer Token & API Key Generation

**Bearer authentication** (also called **token authentication**) is an HTTP **authentication** scheme that involves security **tokens** called **bearer tokens**. Postman uses bearer authentication.

To generate the token, navigate to `Settings` and click on `Generate API key` and copy the key.

![](https://1981680851-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MAQH3DF49Lq0AJudrbF%2Fuploads%2FjJsBFXqPldqbpTv6JqPJ%2FScreenshot%202023-02-24%20at%203.13.56%20PM.png?alt=media\&token=7dcd58ed-52ae-4aff-93ae-9ab8702ab8d0)

![](https://1981680851-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MAQH3DF49Lq0AJudrbF%2Fuploads%2Fl8qPjaF3eiNIrt0Zo8Op%2FScreenshot%202023-04-05%20at%2010.53.38%20AM.png?alt=media\&token=ba47bc2a-ca93-4ec8-b66c-b6d9affebca4)

Enter the API key label and click on "Generate Key"

![](https://1981680851-files.gitbook.io/\~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MAQH3DF49Lq0AJudrbF%2Fuploads%2FJ2ztqOOvyBfcaV0gdLfI%2FScreenshot%202023-04-05%20at%2010.54.31%20AM.png?alt=media\&token=ce699a50-6ed6-4614-8d1e-cdd18cb6ba89)

Copy the newly created API key

**Keep the bearer token** **safe:** You should not share the bearer token with anyone. Use services like 1Password to store it.

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
