## Descripción
Find the flag being held on this server to get ahead of the competition

http://wily-courier.picoctf.net:58861/

INSTANCE

Expires in 26:55Restart Instance

HINTS
1
Maybe you have more than 2 choices
2
Check out tools like Burpsuite to modify your requests and look at the responses
## Solución
```
ReyLuis-academy@webshell:~$ curl -I http://wily-courier.picoctf.net:58861/
HTTP/1.1 200 OK
Date: Wed, 09 Sep 2026 01:01:19 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8
```
En base a que no se puede desde chrome cambiar el metodo de solicitud, lo forzamos con la terminal y aparece nuestra bandera
## Notas adicionales

## Referencias
https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Methods