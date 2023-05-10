# Attachments

Our programmatic email API supports attachments via [`multipart/form-data` requests](https://www.w3.org/TR/html401/interact/forms.html#h-17.13.4.2).

Please note the following rules when sending attachments:

* The attachment feature is only available to users who have [configured custom domain](../custom-domain-setup.md). If you'd like to configure the emails to send from your own domain, [contact us](https://go.gov.sg/postman-contact-us).
* Each email can have up to 10 attachments
* Each attachment should not exceed 2MB in size
* The cumulative size of all attachments should not exceed 10MB
* You can file the list of supported attachment file types below

<details>

<summary><strong>List of supported attachment file types</strong></summary>

* `asc`
* `avi`
* `bmp`
* `csv`
* `dgn`
* `docx`
* `dwf`
* `dwg`
* `dxf`
* `ent`
* `gif`
* `jpeg`
* `jpg`
* `mpeg`
* `mpg`
* `mpp`
* `odb`
* `odf`
* `odg`
* `ods`
* `pdf`
* `png`
* `pptx`
* `rtf`
* `sxc`
* `sxd`
* `sxi`
* `sxw`
* `tif`
* `tiff`
* `txt`
* `wmv`
* `xlsx`

</details>

## Sample API calls

### API call with one attachment

```zsh
curl --location --request POST 'https://api.postman.gov.sg/v1/transactional/email/send' \
--header 'Authorization: Bearer your_api_key' \
--form 'body="<p>Hello <b>there</b></p>"' \
--form 'recipient="user@agency.gov.sg"' \
--form 'attachments=@"/your/local/path-to-file"' \
--form 'subject="Test email"'
```

### API call with two attachments

```zsh
curl --location --request POST 'https://api.postman.gov.sg/v1/transactional/email/send' \
--header 'Authorization: Bearer your_api_key' \
--form 'body="<p>Hello <b>there</b></p>"' \
--form 'recipient="user@agency.gov.sg"' \
--form 'attachments=@"/your/local/path-to-file-1"' \
--form 'attachments=@"/your/local/path-to-file-2"' \
--form 'subject="Test email"'
```