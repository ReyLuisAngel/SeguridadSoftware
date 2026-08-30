## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2026-08-26 16:49:37--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                                                 100%[==================================================================================================================================>]     876  --.-KB/s    in 0s      

2026-08-26 16:49:37 (257 MB/s) - 'level1.py' saved [876/876]

ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2026-08-26 16:49:50--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc                                       100%[==================================================================================================================================>]      30  --.-KB/s    in 0s      

2026-08-26 16:49:50 (561 KB/s) - 'level1.flag.txt.enc' saved [30/30]

ReyLuis-academy@webshell:~$ nano level1.py
ReyLuis-academy@webshell:~$ nano level1.py
ReyLuis-academy@webshell:~$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
ReyLuis-academy@webshell:~$ 
```
Entramos con nano al programa ejecutable de python y observamos dentro del programa cual era la contraseña necesaria para que nos diera la respuesta correcta.
## Notas adicionales

## Referencias
