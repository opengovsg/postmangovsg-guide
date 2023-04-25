---
description: >-
  This page is still under construction, if you do not find the answer to your
  question, please reach out to us directly
---

# API FAQ

## How to set up custom domain?

The following steps described the process of setting up custom domain on PostmanSG.

1. **Email or submit a** [**form**](https://go.gov.sg/postman-contact-us) **to PostmanSG team,** let us know that you intend to customise your domain with the following information:
   * Your use case (if you have not shared with PostmanSG team previously)
   * The email address that you intend to send your email out from (e.g no-reply@agency.gov.sg)
   * If you have a launch timeline, please also inform us ahead for us to prioritise your request
2. **PostmanSG will generate and send agency DKIM records**&#x20;
   * This may take a few days to a week depending on our availability. So do remember to share your timeline if you have any.&#x20;
3. **Agency to add DKIM records in your DNS**.
   *   Create CNAME records in DNS (ITSM/DNS Provider) and add the DKIM files.

       \
       _If you do not have access to your DNS records, you should speak to your ITD who has access to your agency domain (this is the domain that you want to send the email from, e.g_ [_ica.gov.sg_](http://ica.gov.sg)_) on ITSM._
4. **PostmanSG to add the specified sender email into our database.**
   * PostmanSG will inform agency once this step is done
5. **Agency to verify if the configuration works.**
   * PostmanSG uses Amazon SES, which may take up to 72 hours to complete the verification process in Step 2.\
     \
     To check if you the domain configuration is done, you can either try sending an email using API or log into [PostmanSG](http://postman.gov.sg/) portal and see if you are able to select your custom domain e.g ([do\_not\_reply@ica.gov.sg](mailto:do\_not\_reply@ica.gov.sg)) to send your campaign.
6. **If you require your emails to be receivable to .gov.sg emails**
   * Most agency domains would have been whitelisted on PostmanSG but if you would like confirmation, you may reach the team separately on this.
