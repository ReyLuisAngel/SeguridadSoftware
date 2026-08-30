## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/179/challenge.zip)

HINTS

1

`git branch -a` will let you see available branches
## Solución
```
ReyLuis-academy@webshell:~$ cd drop-in/
ReyLuis-academy@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/ReyLuis-academy/drop-in/.git/
ReyLuis-academy@webshell:~/drop-in$ git branches -a
git: 'branches' is not a git command. See 'git --help'.
ReyLuis-academy@webshell:~/drop-in$ git branch -a
ReyLuis-academy@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
ReyLuis-academy@webshell:~/drop-in$ ls
flag.py
ReyLuis-academy@webshell:~/drop-in$ nano flag.py
ReyLuis-academy@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
ReyLuis-academy@webshell:~/drop-in$ nano flag.py 
```
Con la pista para ver las ramas podemos cambiar con checkout de rama para ver como nuestro archivo de flag.py cambiaba en cada una de las 3 ramas completando nuestra bandera poco a poco.
## Notas adicionales
`git branch -a` will let you see available branches
## Referencias
