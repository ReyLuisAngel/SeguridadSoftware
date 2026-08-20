## Descripción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?

Connect to fickle-tempest.picoctf.net 65335.
## Solución
La solución era utilizar 
```
ReyLuis-academy@webshell:~$ nc fickle-tempest.picoctf.net 65335 > H
^C
ReyLuis-academy@webshell:~$ ls
H  README.txt  file  flag
ReyLuis-academy@webshell:~$ cat H | grep pico                
picoCTF{digital_plumb3r_00da27CC}

```
Cargamos el archivo como H y como anteriormente haciamos con cat buscamos lo que necesitabamos y salio
## Notas adicionales

## Referencias
https://webshell.cylabacademy.org