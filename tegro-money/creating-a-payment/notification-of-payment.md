# Notification of payment

After payment, a request containing payment information will be sent to the **notification URL** specified in your store settings

<table><thead><tr><th width="412">Key</th><th>Description</th></tr></thead><tbody><tr><td>shop_id</td><td>Project public key</td></tr><tr><td>amount</td><td>Payment amount</td></tr><tr><td>order_id</td><td>Order ID</td></tr><tr><td>currency</td><td>Payment currency (RUB, USD, EUR)</td></tr><tr><td>test</td><td>If it was set at the time of payment</td></tr><tr><td>sign</td><td>Request Signature</td></tr></tbody></table>

The signature is formed in the same way as when a form is created, but all fields are involved in the hash formation, for example

```php
<?php 
$secret = 'GB%^&*YJni677';
$data = $_POST;
unset($data['sign']);
ksort($data);
$str = http_build_query($data);
$sign = md5($str . $secret);
```
