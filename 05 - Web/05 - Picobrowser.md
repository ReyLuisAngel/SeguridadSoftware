## Descripción
This website can be rendered only by picobrowser, go and catch the flag!
## Solución
```
ReyLuis-academy@webshell:~$ curl -s http://fickle-tempest.picoctf.net:53038/flag -H "User-Agent: picobrowser" | grep pico                              
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>
```
buscamos por donde sacar la bandera y era verificando con cual navegador deberiamos entrar asi que buscamos el parametro y le pusimos que somos el navegador de pico
## Notas adicionales

## Referencias
