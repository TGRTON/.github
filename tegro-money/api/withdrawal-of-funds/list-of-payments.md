# List of payments

> **POST** [https://tegro.money/api/withdrawals/](https://tegro.money/api/withdrawals/)

### Request

<table><thead><tr><th width="250.33333333333331">Header</th><th></th><th></th></tr></thead><tbody><tr><td>Authorization</td><td>string</td><td>Request Signature</td></tr></tbody></table>

| Body     |         |                       |
| -------- | ------- | --------------------- |
| shop\_id | string  | Shop ID               |
| nonce    | integer | Unique request number |
| page     | integer | Page                  |
