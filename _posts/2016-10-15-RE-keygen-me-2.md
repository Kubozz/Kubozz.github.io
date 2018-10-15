---
layout: post
title: picoCTF2018
description:  RE keygen me 2 (400)
image: assets/images/picoctf2018_12.PNG
---

This challenge is the same with challenge keygen me 1. It is just different at validate_key() function.
Put it in to IDA pro , after find to validate_key() function. We have like this

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_13.PNG)
Key will thought 12 function to check correct key . 

key_constraint_01()

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_14.PNG)

key_constraint_02()

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_15.PNG)
