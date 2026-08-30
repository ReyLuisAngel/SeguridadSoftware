## Descripción
How to automate tasks to run at intervals on linux servers?

Use ssh to connect to this server:

`Server: saturn.picoctf.net Port: 59509 Username: picoplayer Password: kZx-HVJKu8`
## Solución
```
picoplayer@challenge:~$ crontab -l
no crontab for picoplayer
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ crontab -l
no crontab for picoplayer
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ crontab -l
no crontab for picoplayer
picoplayer@challenge:/$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```
tratando de acceder al crontab -l(lista de tareas del usuario) vimos que no teniamos acceso y al tratar de obtener permisos o ver el crontab de root no se nos permitio asi que observamos que ahi dentro del archivo crontab del sistema que se encontraba dentro de etc y ahi aparecio la bandera
## Notas adicionales
ssh -p 2222 tu_usuario@192.168.1.50
Para ingresar a un servidor ssh primero la leyenda ssh, -p en caso de ir a un puerto en especifico, el usuario con un arroba al final y pegado al arroba la direccion a donde nos vamos a conectar.

## Referencias
https://josephkimiri.github.io/posts/chrono/