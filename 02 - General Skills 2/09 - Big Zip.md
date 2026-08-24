## Descripción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)

HINTS

1-Can grep be instructed to look at every file in a directory and its subdirectories?
## Solución
Primero conseguimos el archivo con wget
Despues usamos el grep para pasar a traves de los archivos buscando la palabra pico
```
grep -r "pico"
```
Pero primero entramos al archivo de lo contrario se podría poner la direccion de donde buscar
## Notas adicionales
grep -r para buscar en archivos y subdirectorios
## Referencias
