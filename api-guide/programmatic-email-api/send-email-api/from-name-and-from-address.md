# From Name and From Address

## From Name vs From Address

The `from` field of an email contains **from name** and **from address**. This is illustrated in the image below:

![](../../../.gitbook/assets/from-name-and-address.png)

If the `from` field in the JSON body of the API call is omitted:

1. The from name defaults to `Postman.gov.sg`
2. The from address defaults to `<donotreply@@mail.postman.gov.sg>`

## Changing From Name

In our API, the from name of an email can be changed by the API user by modifying the `from` field in the API call. For example, to use `New Product` as the from name, the API user could use the following JSON body:

```json
{
  "recipient": "zixiang@open.gov.sg",
  "subject": "Hello there",
  "body": "What's upppp",
  "from": "New Product <donotreply@mail.postman.gov.sg>"
}
```

The email recipient will see the following:

<figure><img src="../../../.gitbook/assets/custom-from-name.png" alt="" width="375"><figcaption></figcaption></figure>

For users that wish to customise their emails without going through the hassle of setting up a [custom from address](../custom-from-address.md), this is an intermediate solution used by our existing users.

## Using a Custom From Address

Users may wish to send emails using a custom from name as well as a custom from address (i.e. any email address that is not the default `<donotreply@mail.postman.gov.sg>`. Setting up a custom from address is necessary; for more information, [see here](../custom-from-address.md).

{% hint style="info" %}
Create an account on Postman using the email address from which you wish to send your email.

For example, if you want your email to be sent from <mark style="color:red;">`no-reply@agency.gov.sg`</mark>, you should log into Postman using this email address and generate your API keys on the dashboard.
{% endhint %}

To make use of the custom from address, the JSON body of the API call is:

```json
{
  "recipient": "zixiang@open.gov.sg",
  "subject": "Hello there",
  "body": "What's upppp",
  "from": "New Product <donotreply@mail.postman.gov.sg>"
}
```

The recipient will see:

1. A custom from name `New Product`
2. A custom from address `<test_admin@postman.gov.sg>`

![](../../../.gitbook/assets/custom-domain.png)
