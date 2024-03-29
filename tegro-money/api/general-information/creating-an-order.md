# Creating an order

> **POST** [https://tegro.money/api/createOrder/](https://tegro.money/api/createOrder/)

Use this method to get a direct link to pay for your order

### Request

<table><thead><tr><th width="329.3333333333333">Header</th><th></th><th></th></tr></thead><tbody><tr><td>Authorization</td><td>string</td><td>Request Signature</td></tr></tbody></table>

| Body            |         |                                    |
| --------------- | ------- | ---------------------------------- |
| shop\_id        | string  | Shop ID                            |
| nonce           | integer | Unique request number              |
| currency        | string  | Payment currency, RUB/USD/EUR etc. |
| amount          | number  | Payment amount                     |
| order\_id       | string  | Your store order number            |
| payment\_system | integer | Payment system ID                  |
| fields          | array   | Customer information               |
| receipt         | array   | Basket data                        |

### Reply

```json
{
  "type": "success",
  "desc": "",
  "data": {
    "id": 755555,
    "url": "https://tegro.money/pay/complete/755555/7f259f856e7682a6e98179036a623696/"
  }
}
```

### Example request

```json
{
  "shop_id": "1913EA935149B1E5D852A",
  "nonce": 1613435880,
  "currency": "RUB",
  "amount": 1200,
  "order_id": "test order",
  "payment_system": 5,
  "fields": {
    "email": "user@email.ru",
    "phone": "79111231212"
  },
  "receipt": {
    "items": [
      {
        "name": "test item 1",
        "count": 1,
        "price": 600
      },
      {
        "name": "test item 2",
        "count": 1,
        "price": 600
      }
    ]
  }
}
```
