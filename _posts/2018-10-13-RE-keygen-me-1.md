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
Open file with IDA pro to see souce code. Found to main function 

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_5.PNG)

Summary program active :
Firstly -> program will check parameter . if parameter < 1 program will show "Please Provide a VALID 16 byte Product Key." else it will call check_valid_key(). This is check_valid_key() code :

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_8.PNG)

The main purpose of check_valid_key() is check characters in the range "0"->"9" and "A" -> "Z".
Next validate_key() function:

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_9.PNG)

The main purpose of this function is check sum of (key[i] * index+i) (i in range 0->14) then take compare sum % 0x24 with key[15]. if equal will show flag.
Ok.. I writed a python script to show Product Key

