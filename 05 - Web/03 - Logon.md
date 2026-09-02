## Descripción
The factory is hiding things from all of its users.

Can you login as Joe and find what they've been looking at? [http://fickle-tempest.picoctf.net:64981](http://fickle-tempest.picoctf.net:64981/)
## Solución
```

```

metodos de soliciud o request metod
utilizamos un cookie editor y vimos que en la cookie había una sección de si era el administrador o no, entonces con el editor cambiamos a true eso y recargando nos tomo como el admin y ahora podemos ver nuestra bandera

consola
abri pagina
inspeccionar
network
ingresamos a un perfil x
se generan las peticiones de la cookie asi que la checamos
ponemos formato raw
copiamos lo de la cookie
y usamos el comando curl -s (direccion del sitio)/flag
-H "lo de la cookie y modificado para que este admin en tru"
| grep pico
y aparece en al consola la Flag
## Notas adicionales
HTML protocolo entre pagina y servidor
request
solicitud
Web cookie es una pequeño fragmento de datos creado por un servidor web

## Referencias
