# PAYPART

**[an iranian payment method for your business]**

you have a business with a website that you need top up the deposit of your users on that with iranian bank accounts.

you can easily connect your users to our server for the payment procedure and we acknowledge you that the payment
was `successful or not` also the `amount of the payment` that your user made it.

## Table of Contents
- [Diagram](#diagram)
- [Config](#how_configure_and_connect_to_this_service)
- [API](#API)
- [Admin](#ADMIN-SIDE)
- [Notes](#notes)
- [our LOGO](#our_logo)

you can see the updates and every new things on this readme page [PayPart Pages](https://github.com/ataeiamirhosein/paypart).

(( for more information and any request you can communicate us trough this mail: info@daryaftamn.shop ))

--------------------------------------------------------------------

## diagram
let first start with a graphical diagram:

![paypart diagram](https://github.com/ataeiamirhosein/paypart/blob/main/assets/images/Paypart.jpg)

## how_configure_and_connect_to_this_service

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

**[ip checker]**
- from the first june of 2025 our server able to check the ip of your user trough the payment process and if the ip of user do not for `Iran` we tell your user that please turn on your VPN.

4- if the result of the payment of your user was succesful we log it in to our databse with your specific TOKEN that you take it before.

--------------------------------------------------------------------

## API

5- you can check the `status of your user` also the `amount of charge` with an **API** on our server trough `POST` method and secure with `https`.

URL:
```
https://daryaftamn.shop/api.php
```
Parameters:
```
token=YOUR_API_KEY
```
```
request=YOUR_USER_ID
```

5.1- if the acknowledge of API was successful this means that your user maid the payment and you received this message:
```JSON
{
  "status": "success",
  "message": "Request found",
  "data": YOUR_USER_AMOUNT
}
```
5.2- if the acknowledge of API was not successful this means that the payment does not occur and you received this message:
```JSON
{
  "status": "error",
  "message": "Request not found in database",
  "data": null
}
```

5.3- you can test simply with [This File](./post.html) our **API** with **POST** method or see the template code here:
```HTML
<form action="https://daryaftamn.shop/api.php" method="POST">
<input type="text" name="token" placeholder="API Token" required>
<input type="text" name="request" placeholder="Request" required>
<button type="submit">Submit</button>
</form>
```

--------------------------------------------------------------------

## ADMIN-SIDE

- you have also an **Management Panel** with your credentials for control your gateways (you can request more than one gateway according to your traffic) also the transaction of your users.

- in your **Management Panel** you can turn on/off your gateway for risk management also.

## notes

- the address of admin panel is:

```
https://daryaftamn.shop/management.php
```

- our server name is:

```
daryaftamn.shop
```

--------------------------------------------------------------------

## our_logo

- you can add [Our LOGO](./assets/images/pp.png) into your website with this template code:

```HTML
<a href="https://daryaftamn.shop"><img src="pp.png" width="75" height="55"></a>
```
