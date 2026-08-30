## Descripción
How well can you perfom basic binary operations?

Start searching for the flag here `nc titan.picoctf.net 51671`
## Solución
```
ReyLuis-academy@webshell:~$ rm * -rf
ReyLuis-academy@webshell:~$ nc titan.picoctf.net 51671

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00011011
Binary Number 2: 10100111


Question 1/6:
Operation 1: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01010011
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 00110110
Correct!

Question 3/6:
Operation 3: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10111111
Correct!

Question 4/6:
Operation 4: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000011
Correct!

Question 5/6:
Operation 5: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0001000110011101
Correct!

Question 6/6:
Operation 6: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11000010
Correct!

Enter the results of the last operation in hexadecimal: C2

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d9a7ddd2}



```
Entrar realizar las operaciones y sale la bandera sola
## Notas adicionales
">>" este simbolo significa desplazamiento a la derecha osea descartar el ultimo digito de la derecha y recorrer todo
"<<" este simbolo significa desplazamiento a la izquierda osea descartar el ultimo digito de la izquierda y recorrer todo
" | " este simbolo es el or por ejemplo 101 | 010 da como resultado 111 porque en cada posicion en ambos numeros al menos hay un 1
"&" es el and y es la misma logica de posiciones
" * " es pasar a decimal los numeros y realizar una multiplicacion despues de ello el resultado de decimal lo conviertes a binario y lo dejas representado en este caso como 2 bits osea rellenas segun los bits faltantes.
" + " para la sumatoria se puede hacer lo mismo a decimal operacion y resultado a binario o hacer lo de acarreo para sumas binarias 
## Referencias
https://gchq.github.io/CyberChef/#recipe=To_Binary('None',8)&input=NTk&ieol=CRLF&oeol=CRLF