---
layout: post
title: picoCTF2018
description:  RE keygen me 2 (750)
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

All function next the same with function 1 and 2. so I don't show it at here.
I will solve it with Z3. I writed a script to solve :
<script src="https://gist.github.com/Kubozz/4b74d92a04fa69261bed5e6e45d27d86.js"></script>
The result:

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_16.PNG)
