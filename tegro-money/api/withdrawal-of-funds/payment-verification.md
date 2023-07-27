# Payment verification

> **POST** [https://tegro.money/api/withdrawal/](https://tegro.money/api/withdrawal/)

### Request

| Header        |        |                   |
| ------------- | ------ | ----------------- |
| Authorization | string | Request Signature |

| Body        |         |                            |
| ----------- | ------- | -------------------------- |
| shop\_id    | string  | Shop ID                    |
| nonce       | integer | Unique request number      |
| order\_id   | integer | Payment number tegro.money |
| payment\_id | string  | or store payment number    |
