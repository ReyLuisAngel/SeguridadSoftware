## Descripción
Can you make sense of this file?

Download the file [here](https://artifacts.picoctf.net/c/476/enc_flag).

HINTS

1-Multiple decoding is always good.
## Solución
Con uno de los comandos de cat podemos decodificar una y otra y otra vez hasta que el resultado sea nuestra bandera
```
ReyLuis-academy@webshell:~$ ls
-h.ltdis.x86_64.txt  -j.ltdis.x86_64.txt  Addadshashanammu  Addadshashanammu.zip  H  README.txt  enc_flag  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
ReyLuis-academy@webshell:~$ cat enc_flag | base64 --decode | base64 --decode
V1RCa2MyRnRTWGRVYkZaVFltNVNjRmRXYUU5aVJUVnhWVzFhYVdGck5UWmFSVkpQWVRGbmVWVnVR
bHBsYTBweVUxWmpNRTVHWjNsVgpXR1JyVFdwV2VsUlZVbE5oTURCNVZXMWFUd3BTUmxWNFZHcEtW
MkZyTUhsV2FteEVXbm93T1VOblBUMEsK
ReyLuis-academy@webshell:~$ ^C
ReyLuis-academy@webshell:~$ cat enc_flag | base64 --decode | base64 --decode | base64 --decode
WTBkc2FtSXdUbFZTYm5ScFdWaE9iRTVxVW1aaWFrNTZaRVJPYTFneVVuQlpla0pyU1ZjME5GZ3lV
WGRrTWpWelRVUlNhMDB5VW1aTwpSRlV4VGpKV2FrMHlWamxEWnowOUNnPT0K
ReyLuis-academy@webshell:~$ cat enc_flag | base64 --decode | base64 --decode | base64 --decode | base64 --decode
Y0dsamIwTlVSbnRpWVhObE5qUmZiak56ZEROa1gyUnBZekJrSVc0NFgyUXdkMjVzTURSa00yUmZO
RFUxTjJWak0yVjlDZz09Cg==
ReyLuis-academy@webshell:~$ cat enc_flag | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNDU1N2VjM2V9Cg==
ReyLuis-academy@webshell:~$ cat enc_flag | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode | base64 --decode
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_4557ec3e}
```
## Notas adicionales

## Referencias
https://medium.com/@omstaendlig/picoctf-writeup-repetitions-e37aa158416d