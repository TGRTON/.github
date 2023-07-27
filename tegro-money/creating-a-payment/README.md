# 💵 Creating a payment

With Tegro.money, both the seller and the buyer get an "electronic cashier," which greatly simplifies transactions and speeds up payments.

To create a payment, you need to pass the necessary parameters to a special url [https://tegro.money/pay/?params](https://tegro.money/pay/?params)

### Mandatory parameters

<table><thead><tr><th width="239">Key</th><th>Description</th></tr></thead><tbody><tr><td>shop_id</td><td>Project public key</td></tr><tr><td>amount</td><td>Payment amount</td></tr><tr><td>order_id</td><td>Order ID (payment number or customer email)</td></tr><tr><td>currency</td><td>Payment currency (RUB, USD, EUR)</td></tr><tr><td>sign</td><td>Request Signature</td></tr></tbody></table>

### Additional parameters

<table><thead><tr><th width="220">Key</th><th>Description</th></tr></thead><tbody><tr><td>lang</td><td>Interface language (ru, en)</td></tr><tr><td>test</td><td>If it is set to "1" - payment will be made in test mode</td></tr><tr><td>payment_system</td><td>Payment system ID</td></tr><tr><td>success_url</td><td>Success url</td></tr><tr><td>fail_url</td><td>Error url</td></tr><tr><td>notify_url</td><td>Notification url</td></tr></tbody></table>

To form a signature, sort all mandatory parameters by key, join key/value pairs with the & symbol and add your secret key to the end. Then make a hash of the resulting MD5 string, for example:

```php
<?php 
$secret = 'GB%^&*YJni677';
$data = array(
    'shop_id'=>'D0F98E7D7742609DC508D86BB7500914',
    'amount'=>100,
    'currency'=>'RUB',
    'order_id'=>'123',
);
ksort($data);
$str = http_build_query($data);
$sign = md5($str . $secret);
```

**Warning!** If the test payment flag test=1 was passed to the payment form, this parameter also takes part in the signature formation:

```php
<?php 
$secret = 'GB%^&*YJni677';
$data = array(
    'shop_id'=>'D0F98E7D7742609DC508D86BB7500914',
    'amount'=>100,
    'currency'=>'RUB',
    'order_id'=>'123',
    'test'=>1,
);
ksort($data);
$str = http_build_query($data);
$sign = md5($str . $secret);
```

It is possible to go directly to the payment system, if you are ready to pass all the data for payment in the incoming request. To do this, send the data by POST to the url [https://tegro.money/pay/form/](https://tegro.money/pay/form/) be sure to specify the parameter payment\_system and pass all the mandatory fields for this method of payment. In most cases this is email, for more information contact support.

Example:

```html
<form action="https://tegro.money/pay/form/" method="post">
<input type="hidden" name="shop_id" value="D0F98E7D7742609DC508D86BB7500914">
<input type="hidden" name="amount" value="100">
<input type="hidden" name="order_id" value="123">
<input type="hidden" name="lang" value="ru">
<input type="hidden" name="currency" value="RUB">
<input type="hidden" name="payment_system" value="11">
<input type="hidden" name="fields[email]" value="user@site.ru">
<input type="hidden" name="sign" value="e51845e62b106d245cc96c431d8aae42">
<input type="submit" value="Pay">
</form>
```
