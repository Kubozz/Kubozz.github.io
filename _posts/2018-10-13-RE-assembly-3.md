---
layout: post
title: picoCTF2018
description: RE assembly 3 Points 400
image: assets/images/pic01.jpg
---

At this challenge , We have a file asm :
  
![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_1.PNG)

With three paramater for function asm3(0xb3fb1998,0xfe1a474d,0xd5373fd4).
we have the stack frame will be like this:

![test image]({{ site.url | absolute_path}}/assets/images/picoctf2018_2.PNG)

Firstly, instruction mov eax,0x62 -> eax=0x00000062 -> al=0x62, ah=0x00

Next,                 xor al,al    -> al=0 -> eax=0x00000000

Next                  mov ah,BYTE PTR [ebp+0xa] -> ah = 19 -> ax= 0x1900

Next                  sal	ax,0x10 ->  left shifts ax -> ax=0x0000

Next                  sub	al,BYTE PTR [ebp+0xd] -> al = 0x00-0x47 = 0xb9

Next                  add	ah,BYTE PTR [ebp+0xe] -> ah = 0x00+0x1a = 0x1a

Next                  xor	ax,WORD PTR [ebp+0x10] -> ax=0x1ab9 xor 0x3fd4 = 0x256d

The result for this challenge is 0x256d





