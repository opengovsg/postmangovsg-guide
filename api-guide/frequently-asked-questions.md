# Frequently Asked Questions

## What is the the cost of using Postman's Programmatic Email API?

There is no cost for agencies to use Postman. OGP absorbs the infrastructure cost and the product is built and maintained in-house.

## Can I use Postman Programmatic Email API to send emails to Intranet recipients?

Yes. We work with SG-Mail to ensure that our emails can be delivered to Intranet recipients. For more information, [see here](programmatic-email-api/sg-mail-whitelisting.md).

## Can I use my Intranet application to call Postman Programmatic Email API?

As Postman is hosted on the Internet, there is ongoing work being done to allow Intranet applications to call our API. For more information, [see this](overview/connecting-your-intranet-application.md).

If your application is hosted on GCC2.0 or on commercial services, your application can call our API.

## How do I know if an email has been sent successfully?

A successful call to our API initiates the email sending process and does not guarantee that the email has been sent or delivered successfully. For more information, [see this](programmatic-email-api/send-email-api/#status-code).

Currently, you can query an email based on its ID to get its up-to-date status. For more information, [see this](programmatic-email-api/get-email-by-id-api.md).

## Can I use Postman Programmatic Email API to mass send emails?

Currently, the API is designed to send one email per API call. As long as the user stays below their [rate limit](programmatic-email-api/send-email-api/rate-limit.md), the user can use it to mass send emails.

## Can I receive monthly reports showing the usage of the APIs by systems per month?

We currently do not have this feature but are actively exploring it. For more information, check out [this section](programmatic-email-api/send-email-api/email-tagging-and-classification.md#email-tagging) of the guide.

## Are there any limitations on the design of the emails?&#x20;

Our API is designed to accommodate a range of use cases. However, we do limit the size of the email body and apply HTML sanitisation. For more information, [see this](programmatic-email-api/send-email-api/email-body/).

## What is the onboarding process?

If you are interested in exploring our API and want to see if your use case is suitable, feel free to reach out to the Postman team via this [form](https://form.gov.sg/#!/62b19812ff209e00126f2c47) so that we can arrange a chat with you.

If you would like to try out the API integration straightaway, you can generate your own API key by logging into your Postman account. Steps to do so are available [here](https://guide.postman.gov.sg/\~/changes/pv1f3DWM1ORa7R0uNLij/api-guide/api-key-management/generate-your-api-key) and our Swagger docs [here](https://api.postman.gov.sg/docs/#/), . Note that there is no test or production environment, you can use our production environment to send your test emails as well.

## What is Postman Programmatic Email API's product roadmap?



## Does each agency definitely need a custom domain email address?

If you are sending attachments in your API emails, then a custom domain is necessary. If you would like your emails to retain your agency branding in the email sender address, then you might also want to consider setting up a custom domain. See [here](https://guide.postman.gov.sg/api-guide/programmatic-email-api/custom-from-address#why-custom-from-address) for more information on custom domain set up, and let us know to kickstart the set-up process for you by filling in this [form](https://form.gov.sg/#!/62b19812ff209e00126f2c47).

