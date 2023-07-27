# Transmitting order information

In some cases, the payment form needs to send data on the composition of the order, such as the name of the product/service, quantity and cost. To do this, include the **receipt** parameter in the request, for example:

```html
<form action="https://tegro.money/pay/form/" method="post">
<input type="hidden" name="shop_id" value="D0F98E7D7742609DC508D86BB7500914">


<!-- Product 1 -->
<input type="hidden" name="receipt[items][0][name]" value="Example of service">
<input type="hidden" name="receipt[items][0][count]" value="1">
<input type="hidden" name="receipt[items][0][price]" value="20">

<!-- Product 2 -->
<input type="hidden" name="receipt[items][1][name]" value="Example of service 2">
<input type="hidden" name="receipt[items][1][count]" value="2">
<input type="hidden" name="receipt[items][1][price]" value="40">


<!-- the total amount of payment must be equal to the sum of all goods! -->
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

**Warning!** This form should be sent to our payment url by **POST** method
