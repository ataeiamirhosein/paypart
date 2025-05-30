# paypart [an iranian payment method for your business]

you have a business with a website that you need top up the deposit of your users on that with iranian bank accounts.

you can easily connect your users to our server for the payment procedure and we acknowledge you that the payment
was `successful or not` also the `amount of the payment` that your user made it.

you can see the updates and every new things on this readme page [PayPart Pages](https://github.com/ataeiamirhosein/paypart).

--------------------------------------------------------------------

let first start with a graphical diagram:

![paypart diagram](https://github.com/ataeiamirhosein/paypart/blob/main/assets/images/Paypart.jpg)

## how configure and connect to this service

0- start with take a TOKEN from us for your business.

1- Consider an `userid` for your user because you should communicate with our server with userid of each of your users.

```PHP
$userid = $conn->query($sql);
```
2- add two other payment method to your website as `C2C` and `Gateway` near your other methods like VISA/MASTER or AMEX.

you can use this simple template code for your self:

```HTML
<a href="https://daryaftamn.shop/gate.php?id=<?php echo $userid; ?>">
<button>GateWay</button></a>

<a href="https://daryaftamn.shop/c2c.php?id=<?php echo $userid; ?>">
<button>C2C</button></a>
```
- now you send your user to our server for the payment

3- your user do the payment procedure.

4- if the result of the payment of your user was succesful we log it in to our databse with your specific TOKEN that you take it before.

5- you can check the `status of your user` also the `amount of charge` with an **API** of our server.

```
https://daryaftamn.shop/api.php?token=YOUR_API_KEY&request=YOUR_USER_ID
```

--------------------------------------------------------------------

- note:
our server name is:

```
daryaftamn.shop
```
