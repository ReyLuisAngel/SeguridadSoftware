## Descripción
Run the Python script and convert the given number from decimal to binary to get the flag.

[Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2026-08-26 16:28:47--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.95, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                              100%[==================================================================================================================================>]   1.16K  --.-KB/s    in 0s      

2026-08-26 16:28:47 (58.9 MB/s) - 'convertme.py' saved [1189/1189]

ReyLuis-academy@webshell:~$ python3 convertme.py
If 87 is in decimal base, what is it in binary base?
Answer: 111011
59 and 87 are not equal.
ReyLuis-academy@webshell:~$ python 
Python 3.10.12 (main, Mar  3 2026, 11:56:32) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(87)
'0b1010111'
>>> 
KeyboardInterrupt
>>> X
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'X' is not defined
>>> exit
Use exit() or Ctrl-D (i.e. EOF) to exit
>>> 
ReyLuis-academy@webshell:~$ ^C
ReyLuis-academy@webshell:~$ python3 convertme.py
If 68 is in decimal base, what is it in binary base?
Answer: 1000100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
```
Descargamos el archivo lo ejecutamos y utilizamos un convertidor de decimal a binario para obtener el numero que nos pedía, y salía sola la bandera
## Notas adicionales

## Referencias
https://www.rapidtables.com/convert/number/decimal-to-binary.html?x=68