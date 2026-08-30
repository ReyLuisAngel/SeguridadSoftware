## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/3/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/3/codebook.txt)
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/3/code.py
--2026-08-26 16:21:05--  https://artifacts.picoctf.net/c/3/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.95, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                                   100%[==================================================================================================================================>]   1.25K  --.-KB/s    in 0s      

2026-08-26 16:21:05 (807 MB/s) - 'code.py' saved [1278/1278]

ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/3/codebook.txt
--2026-08-26 16:21:22--  https://artifacts.picoctf.net/c/3/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                              100%[==================================================================================================================================>]      27  --.-KB/s    in 0s      

2026-08-26 16:21:22 (477 KB/s) - 'codebook.txt' saved [27/27]

ReyLuis-academy@webshell:~$ ls
-h.ltdis.x86_64.txt  Addadshashanammu      H           big-zip-files      code.py       enc_flag  files      flag      runme.py  static.ltdis.strings.txt  strings
-j.ltdis.x86_64.txt  Addadshashanammu.zip  README.txt  big-zip-files.zip  codebook.txt  file      files.zip  ltdis.sh  static    static.ltdis.x86_64.txt   warm
ReyLuis-academy@webshell:~$ python3 code.py                               
picoCTF{c0d3b00k_455157_197a982c}
ReyLuis-academy@webshell:~$ 


```
Después de obtener los 2 archivos ejecutamos uno, y sale la bandera sola, pero se necesitaban los dos porque uno de los código sustraía la contraseña del otro.
## Notas adicionales
También se podía usar nano un editor de archivos que se puede usar en linux.

## Referencias
