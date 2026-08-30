## Descripción
Someone's commits seems to be preventing the program from working. Who is it?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/157/challenge.zip)

HINTS
1
In collaborative projects, many users can make many changes. How can you see the changes within one file?
2
Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3
You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
## Solución
```
ReyLuis-academy@webshell:~$ ls
challenge.zip  drop-in
ReyLuis-academy@webshell:~$ cd drop-in
ReyLuis-academy@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/ReyLuis-academy/drop-in/.git/
ReyLuis-academy@webshell:~/drop-in$ git log message.py
ReyLuis-academy@webshell:~/drop-in$ 
```
Se realiza lo mismo que el anterior pero en este caso una de las pistas hablaba de ver quien hizo los cambios en un determinado archivo dudandolo introduje git log (nombre del archivo) y ahi estaba la bandera
## Notas adicionales

## Referencias
