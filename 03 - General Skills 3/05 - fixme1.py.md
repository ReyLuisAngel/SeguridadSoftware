## Descripción
Fix the syntax error in this Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2026-08-26 16:37:20--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                                 100%[==================================================================================================================================>]     837  --.-KB/s    in 0s      

2026-08-26 16:37:21 (39.6 MB/s) - 'fixme1.py' saved [837/837]

ReyLuis-academy@webshell:~$ python3v fixme1.py
-bash: python3v: command not found
ReyLuis-academy@webshell:~$ cat fixme1.py

import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr(0x5a) + chr(0x1d) + chr(0x1d) + chr(0x2a) + chr(0x06) + chr(0x1c) + chr(0x5a) + chr(0x5c) + chr(0x55) + chr(0x40) + chr(0x3a) + chr(0x58) + chr(0x0a) + chr(0x5d) + chr(0x53) + chr(0x43) + chr(0x06) + chr(0x56) + chr(0x0d) + chr(0x14)

  
flag = str_xor(flag_enc, 'enkidu')
  print('That is correct! Here\'s your flag: ' + flag)

ReyLuis-academy@webshell:~$ nano -l ^C
ReyLuis-academy@webshell:~$ nano -l fixme1.py
ReyLuis-academy@webshell:~$ python3v fixme1.py
-bash: python3v: command not found
ReyLuis-academy@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
Utilizamos nano para entrar al archivo y corregir el problema que tenia, al volverlo a correr apareció sola la bandera
## Notas adicionales

## Referencias
