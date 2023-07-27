# Order verification

> **POST** [https://tegro.money/api/order/](https://tegro.money/api/order/)

Getting information about the order

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

### Reply

```json
{
  "type": "success",
  "desc": "",
  "data": {
    "id": 1232,
    "date_created": "2020-11-14 23:32:37",
    "date_payed": "2020-11-14 23:33:39",
    "status": 1,
    "payment_system_id": 10,
    "currency_id": 1,
    "amount": "64.18000000",
    "fee": "4.00000000",
    "email": "user@site.ru",
    "test_order": 0,
    "payment_id": "Order #17854"
  }
}
```

### Example request

```json
{
  "shop_id": "1913EA935149B1E5D852A",
  "nonce": 1613435880,
  "payment_id": "test order"
}
```
