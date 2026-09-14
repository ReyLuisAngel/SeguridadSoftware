## Descripción
Check the admin scratchpad!
[http://fickle-tempest.picoctf.net:61109](http://fickle-tempest.picoctf.net:61109/)
HINTS
1
What is that cookie?
2
Have you heard of JWT?
## Solución
```
Entramos a un sitio raro donde podemos loguear excepto con admin
Buscando y viendo como jwt es conformado buscamos entrar como admin  para buscar el token utilizamos un crecker llamado jhon que ya esta instalado en ubuntu
```
modificando la cookie vimos que podemos modificar el jwt y cambiando la palabra clave para admin en este caso ilovepico en jwt, pudimos entrar y obtener la bandera.
## Notas adicionales

## Referencias
https://jwt.lannysport.net   pagina jwt para editar el token jwt