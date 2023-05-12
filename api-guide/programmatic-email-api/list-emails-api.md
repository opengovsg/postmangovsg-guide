# List Emails API

This API allows you to retrieve previously sent emails.

{% swagger src="https://api.postman.gov.sg/openapi.yaml" path="/transactional/email" method="get" %}
[https://api.postman.gov.sg/openapi.yaml](https://api.postman.gov.sg/openapi.yaml)
{% endswagger %}

## Response Format

The response is a JSON object with the following fields:

- `has_more`: a boolean indicating whether there are more emails to retrieve
- `data`: an array of JSON email objects. You can find an example of a single JSON email object [here](./get-email-by-id-api.md#example-response).

## Supported Query Parameters

### Limit

You can specify the number of emails to return per page using the `limit` query parameter. The default value is 10, the minimum value is 1, and the maximum value is 100.

### Offset

You can specify the number of emails to skip using the `offset` query parameter. The default value is 0.

### Filtering

We currently support the following filters:

- `status`: return emails with the specified status. For a list of possible values, see [this section](./tracking-email-status.md#email-status)
- `created_at`: return emails created within the specified time range; this roughly corresponds to the time when the API call to send the email was made.

For `created_at`, the timestamp should be specified in valid [ISO 8601 format](https://en.wikipedia.org/wiki/ISO_8601). The list of supported operators are:

- `gt`: greater than
- `gte`: greater than or equal to
- `lt`: less than
- `lte`: less than or equal to

### Sorting

The default sorting option is `created_at`, descending.

We currently support the following sorting options:

- `created_at`: sort by the time when the email was created; this roughly corresponds to the time when the API call to send the email was made
- `updated_at`: sort by the time when the email was last updated

We support both ascending and descending order.

To specify the order, add the prefix `+` for ascending order and `-` for descending order. For example, `+created_at` will sort by `created_at` in ascending order, and `-updated_at` will sort by `updated_at` in descending order. If the prefix is omitted, descending order will be used.

## Example Queries

### `GET /transactional/email`

Returns the first 10 emails sorted by `created_at` in descending order

### `GET /transactional/email?limit=20&offset=10`

Returns the next 20 emails sorted by `created_at` in descending order

### `GET /transactional/email?status=DELIVERED`

Returns the first 10 emails with status `DELIVERED` sorted by `created_at` in descending order

### `GET /transactional/email?created_at[gt]=2023-05-10T03:03:54.163Z`

Returns the first 10 emails created after `2023-05-10T03:03:54.163Z` sorted by `created_at` in descending order. Do note that if the timezone is not specified, it will be assumed to be UTC.

### `GET /transactional/email?created_at[gt]=2023-05-03&created_at[lt]=2023-05-10`

Returns the first 10 emails created between `2023-05-03` and `2023-05-10` sorted by `created_at` in descending order.

### `GET /transactional/email?sort_by=+created_at&created_at[gte]=2022-11-01&status=delivered&limit=48`

Returns the first 48 emails with status `DELIVERED` created on or after `2022-11-01` sorted by `created_at` in ascending order.
