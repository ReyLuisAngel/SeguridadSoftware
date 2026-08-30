## Descripción
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/75/challenge.zip)

HINTS
1
Version control can help you recover files if you change or lose them!

2
Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)

3
You can 'checkout' commits to see the files inside them
## Solución
```
ReyLuis-academy@webshell:~$ cd drop-in
ReyLuis-academy@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/ReyLuis-academy/drop-in/.git/
ReyLuis-academy@webshell:~/drop-in$ git log
ReyLuis-academy@webshell:~/drop-in$ git checkout 6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2
Note: switching to '6603cb4ff0c4ea293798c03a32e0d78d5ab12ca2'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 6603cb4 create flag
ReyLuis-academy@webshell:~/drop-in$ cat message.txt
picoCTF{s@n1t1z3_9539be6b}
ReyLuis-academy@webshell:~/drop-in$ 
```
Descargamos y extraemos el archivo y con eso nos vamos a la carpeta de drop-in no se porque pero solo ahi dentro es donde funcionan los comandos de git
dentro de la carpeta iniciamos el git buscamos en el log el historial y con checkout restauramos esa instancia de trabajo y ahora si vemos el archivo de message.txt donde esta la bandera.
## Notas adicionales

## Referencias
https://medium.com/@hibabintefaheem/commitment-issues-picoctf-beginners-walkthrough-writeup-76979f2b63d0