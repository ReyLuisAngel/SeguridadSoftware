## Descripción
Find the flag in the Python script!

[Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
## Solución
```
ReyLuis-academy@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
--2026-08-26 17:07:36--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py                                             100%[==================================================================================================================================>]   2.49K  --.-KB/s    in 0s      

2026-08-26 17:07:36 (35.9 MB/s) - 'serpentine.py' saved [2550/2550]

ReyLuis-academy@webshell:~$ nano serpentine.py 
ReyLuis-academy@webshell:~$ python3 serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
```
Descargamos y entramos con nano, con pistas dentro del código forzamos a que utilizara la función para imprimir la bandera y ejecutándolo otra vez apareció la bandera.
## Notas adicionales

## Referencias
