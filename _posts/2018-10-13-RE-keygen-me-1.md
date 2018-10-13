---
layout: post
title: picoCTF2018
description: RE keygen me 1 (400)
image: assets/images/picoctf2018_4.PNG
---
This challenge is give we a file like this:

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_6.PNG)
That is a file ELF 32-bit  LSB executable,
ok..try run it.

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_7.PNG)

The program is request a parameter . This parameter must lenght is 16 byte . So we need input 16 character for this file. if this input correct then program will show flag.




