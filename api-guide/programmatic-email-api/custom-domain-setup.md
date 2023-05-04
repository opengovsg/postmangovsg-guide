# Custom Domain Setup

{% hint style="warning" %}
This page is under construction.
{% endhint %}

## What is it?

By default, your emails will be sent from donotreply@mail.postman.gov.sg domain.

If you would like to send through your own email domain, there are additional configurations you need to do on your DNS.

## How to set up custom domain?

The following steps described the process of setting up custom domain on Postman.

1. **Email or submit a** [**form**](https://go.gov.sg/postman-contact-us) **to Postman team,** let us know that you intend to customise your domain with the following information:
   * Your use case (if you have not shared with Postman team previously)
   * The email address that you intend to send your email out from (e.g `no-reply@agency.gov.sg`)
   * If you have a launch timeline, please also inform us ahead for us to prioritise your request
2. **Postman will generate and send agency DKIM records**
   * This may take a few days to a week depending on our availability. So do remember to share your timeline if you have any.
3. **Agency to add DKIM records in your DNS**.
   * Create CNAME records in DNS (ITSM/DNS Provider) and add the DKIM files.
   * _If you do not have access to your DNS records, you should speak to your ITD who has access to your agency domain (this is the domain that you want to send the email from, e.g_ [_ica.gov.sg_](http://ica.gov.sg)_) on ITSM._
4. **Postman to add the specified sender email into our database.**
   * Postman will inform agency once this step is done
5. **Agency to verify if the configuration works.**
   * Postman uses Amazon SES, which may take up to 72 hours to complete the verification process in Step 2.
   * To check if you the domain configuration is done, you can either try sending an email using API or log into [Postman](http://postman.gov.sg/) portal and see if you are able to select your custom domain e.g  `no-reply@agency.gov.sg` to send your campaign.
6. **If you need to send emails to Intranet .gov.sg emails**
   * Most agency domains would have been whitelisted on Postman but if you would like confirmation, you may reach the team separately on this.
