# Withdrawal of funds

> **POST** [https://tegro.money/api/createWithdrawal/](https://tegro.money/api/createWithdrawal/)

### Request

| Header        |        |                   |
| ------------- | ------ | ----------------- |
| Authorization | string | Request Signature |

| Body            |         |                              |
| --------------- | ------- | ---------------------------- |
| shop\_id        | string  | Shop ID                      |
| nonce           | integer | Unique request number        |
| currency        | string  | Currency RUB / USD / EUR etc |
| account         | string  | Account number for payment   |
| amount          | number  | Amount                       |
| payment\_id     | string  | Output ID                    |
| payment\_system | integer | Payment system               |
