# General Information

## Obtaining an API key

API key for access to Tegro.money REST service can be generated on the store settings page [https://tegro.money/my/shop-settings/](https://tegro.money/my/shop-settings/)

![](<../../../.gitbook/assets/image (55).png>)

All data in requests to Tegro.money service is sent by POST via HTTP protocol to the address https://tegro.money/api/_method._ Parameters of the message are packed into JSON-object.

A signature must be sent along with the request. The whole request body should be signed as it is sent to the Bank's server (after serializing the request body in JSON to send it via HTTP).

> In each query it is necessary to pass a **nonce** parameter different from the previous one! For example, you can use the current time in seconds

Use your secret key for the signature. Generate a signature with SHA-256 algorithm.

```php
<?php

$api_key = 'EEFA1913EA9D9351469B1E5D852A';

$data = array(
    'shop_id' =>'1913EA9D9351469B1E5D852A',
    'nonce' => time(),
);

$body = json_encode($data);
$sign = hash_hmac('sha256', $body, $api_key);


$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://tegro.money/api/orders/",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS =>$body,
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer $sign",
    "Content-Type: application/json"
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```
