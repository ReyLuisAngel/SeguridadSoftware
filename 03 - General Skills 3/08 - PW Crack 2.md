## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.py
--2026-08-26 16:54:06--  https://artifacts.picoctf.net/c/14/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py                                                 100%[==================================================================================================================================>]     914  --.-KB/s    in 0s      

2026-08-26 16:54:06 (29.5 MB/s) - 'level2.py' saved [914/914]

ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
--2026-08-26 16:54:26--  https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc                                       100%[==================================================================================================================================>]      31  --.-KB/s    in 0s      

2026-08-26 16:54:26 (11.6 MB/s) - 'level2.flag.txt.enc' saved [31/31]

ReyLuis-academy@webshell:~$ nano level2.py
ReyLuis-academy@webshell:~$ python
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))
4ec9
>>> 
ReyLuis-academy@webshell:~$ python3 level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
```
Descargamos los archivos entramos con nano y vimos que la contraseña estaba dentro del código pero codificada, utilizando el codificador de python interpretamos y obtuvimos la contraseña  
## Notas adicionales

## Referencias
