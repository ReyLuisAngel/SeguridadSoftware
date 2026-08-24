## Descripción
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
## Solución
buscamos con el grep pico dentro de files que es el archivo que descargamos y unzipeamos
```
ReyLuis-academy@webshell:~$ cd files
ReyLuis-academy@webshell:~/files$ grep -r "pico"
adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}
14789.txt.utf-8:brassa un picotin d'orge_. Comme depuis une demi-heure environ c'était
```
## Notas adicionales

## Referencias
