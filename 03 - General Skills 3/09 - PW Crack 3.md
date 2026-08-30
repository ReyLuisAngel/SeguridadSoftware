## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.

There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
--2026-08-26 16:58:27--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                                 100%[==================================================================================================================================>]   1.31K  --.-KB/s    in 0s      

2026-08-26 16:58:27 (52.2 MB/s) - 'level3.py' saved [1337/1337]

ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2026-08-26 16:58:47--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.18, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                                       100%[==================================================================================================================================>]      31  --.-KB/s    in 0s      

2026-08-26 16:58:47 (478 KB/s) - 'level3.flag.txt.enc' saved [31/31]

ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2026-08-26 16:59:01--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                           100%[==================================================================================================================================>]      16  --.-KB/s    in 0s      

2026-08-26 16:59:01 (225 KB/s) - 'level3.hash.bin' saved [16/16]

ReyLuis-academy@webshell:~$ nano level3.py
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: 87ab
That password is incorrect
ReyLuis-academy@webshell:~$ rm * -rf
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py
--2026-08-26 17:02:01--  https://artifacts.picoctf.net/c/17/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.40, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                                                 100%[==================================================================================================================================>]   1.31K  --.-KB/s    in 0s      

2026-08-26 17:02:01 (495 MB/s) - 'level3.py' saved [1337/1337]

ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
--2026-08-26 17:02:09--  https://artifacts.picoctf.net/c/17/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc                                       100%[==================================================================================================================================>]      31  --.-KB/s    in 0s      

2026-08-26 17:02:09 (20.8 MB/s) - 'level3.flag.txt.enc' saved [31/31]

ReyLuis-academy@webshell:~$ ls
level3.flag.txt.enc  level3.py
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
--2026-08-26 17:02:33--  https://artifacts.picoctf.net/c/17/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.40, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin                                           100%[==================================================================================================================================>]      16  --.-KB/s    in 0s      

2026-08-26 17:02:33 (4.35 MB/s) - 'level3.hash.bin' saved [16/16]

ReyLuis-academy@webshell:~$ nano level3.py
ReyLuis-academy@webshell:~$ tail level3.py



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]

ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: f159
That password is incorrect
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: 3961
That password is incorrect
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: 752e
That password is incorrect
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: dba8
That password is incorrect
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: f09e
That password is incorrect
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: 4dcf
That password is incorrect
ReyLuis-academy@webshell:~$ python3 level3.py 
Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```
Descargamos los archivos y viendo con nano el .py podemos notar que salían las posibles contraseñas, con prueba y error conseguimos que la bandera apareciera 
## Notas adicionales

## Referencias
