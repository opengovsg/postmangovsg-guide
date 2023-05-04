# Attachments


#### Sending attachment through programmatic email API

Postman API allows the sending of attachment. Here are a few things to note:

* Attachment should not exceed 2MB in size
* You can only attach a maximum of 5 attachments per email
* Attachment format must be within the list of file types (see the full list below).
* This is only available to users who has configured custom domain. ie. sending from your own domain. If you'd like to configure the emails to send from your own domain, reach out to [us](https://go.gov.sg/postman-contact-us) to find out more details.

<details>

<summary><strong>List of supported file types</strong></summary>

* asc
* avi
* bmp
* csv
* dgn
* docx
* dwf
* dwg
* dxf
* ent
* gif
* jpeg
* jpg
* mpeg
* mpg
* mpp
* odb
* odf
* odg
* ods
* pdf
* png
* pptx
* rtf
* sxc
* sxd
* sxi
* sxw
* tif
* tiff
* txt
* wmv
* xlsx

</details>

For more details on usage, refer to our Swagger docs [here](https://api.postman.gov.sg/docs/#/Email/post\_transactional\_email\_send)

With 1 attachment

```zsh
curl --location --request POST 'https://api.postman.gov.sg/v1/transactional/email/send' \
--header 'Authorization: Bearer your_api_key' \
--form 'body="<p>Hello <b>there</b></p>"' \
--form 'recipient="user@agency.gov.sg"' \
--form 'attachments=@"/your/local/path-to-file"' \
--form 'subject="Test email"'
```

With multiple attachments

```zsh
curl --location --request POST 'https://api.postman.gov.sg/v1/transactional/email/send' \
--header 'Authorization: Bearer your_api_key' \
--form 'body="<p>Hello <b>there</b></p>"' \
--form 'recipient="user@agency.gov.sg"' \
--form 'attachments=@"/your/local/path-to-file-1"' \
--form 'attachments=@"/your/local/path-to-file-2"' \
--form 'subject="Test email"'
```
