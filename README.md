# paypart [an iranian payment method for your business]

you have a business with a website that you need top up the deposit of your users on that with iranian bank accounts.

you can easily connect your users to our server for the payment procedure and we acknowledge you that the payment
was `successful or not` also the `amount of the payment` that your user made it.

you can see the updates and every new things on this readme page [PayPart Pages](https://github.com/ataeiamirhosein/paypart).

--------------------------------------------------------------------

let first start with a graphical diagram:

![paypart diagram](https://github.com/ataeiamirhosein/paypart/blob/main/assets/images/Paypart.jpg)

## how configure and connect to this service

1- Consider an `userid` for your user because you should communicate with our server with userid of each of your users.

```PHP
$userid = $conn->query($sql);
```
2- add two other payment method to your website as `C2C` and `Gateway` near your other methods like VISA/MASTER or AMEX.

you can use this template code for your self:
```HTML
<a href="https://daryaftamn.shop/gate.php?id=<?php echo $userid; ?>">
<button>GateWay</button></a>

<a href="https://daryaftamn.shop/c2c.php?id=<?php echo $userid; ?>">
<button>C2C</button></a>
```
