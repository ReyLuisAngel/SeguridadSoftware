## Descripción
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

Start your instance to see connection details.

`ssh -p 52031 [ctf-player@saturn.picoctf.net](mailto:ctf-player@saturn.picoctf.net)`

The password is `3f39b042`
## Solución
```
Special$ ${parameter?ls}
${parameter?ls} 
sh: 1: parameter: ls
Special$ ${:ls}
${:ls} 
sh: 1: Bad substitution
Special$ ${parameter=ls}
${parameter=ls} 
blargh
Special$ ${parameter=cat blargh}
${parameter=cat blargh} 
cat: blargh: Is a directory
Special$ ${parameter=cd blargh}
${parameter=cd blargh} 
Special$ ${parameter=ls blargh}
${parameter=ls blargh} 
flag.txt
Special$ ${parameter=cat < blargh/flag.txt}
${parameter=cat < blargh/flag.txt} 
cat: '<': No such file or directory
picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}
```
Osea al parecer nos aventaron a un linux que no tiene designados los comando por lo que con un cierto comando podemos asignar valores
No me equivoque en realidad estamos buscando los valores de los comandos osea tienen otros nombres y preguntandole al programa nos iba dando el valor que debiamos utilizar

## Notas adicionales

## Referencias
https://josephkimiri.github.io/posts/Special/