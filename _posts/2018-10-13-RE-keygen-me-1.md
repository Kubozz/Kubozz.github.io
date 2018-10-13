---
layout: post
title: picoCTF2018
description: RE keygen me 1 (400)
image: assets/images/picoctf2018_4.PNG
---


int __cdecl main(int argc, const char **argv, const char **envp)
{
  int result; // eax

  setvbuf(_bss_start, 0, 2, 0);
  if ( argc > 1 )
  {
    if ( (unsigned __int8)check_valid_key(argv[1]) )
    {
      if ( (unsigned __int8)validate_key((char *)argv[1]) )
      {
        printf("Product Activated Successfully: ");
        print_flag(&argc);
        result = 0;
      }
      else
      {
        puts("INVALID Product Key.");
        result = -1;
      }
    }
    else
    {
      puts("Please Provide a VALID 16 byte Product Key.");
      result = -1;
    }
  }
  else
  {
    puts("Usage: ./activate <PRODUCT_KEY>");
    result = -1;
  }
  return result;
}

