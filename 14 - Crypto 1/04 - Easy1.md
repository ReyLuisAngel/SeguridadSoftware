## Descripción
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://challenge-files.cylabacademy.net/library/14a944b4b00c6d6e9213b62098e0c8a8d77219757b1a51d9af4bc15e263b6b92/table.txt) to solve it?.
Hints
1
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'academy{HELLO}' as the flag.
2
Please use all caps for the message.
## Solución
```
academy{CRYPTOISFUN}
```
Observando dentro del archivo que se nos dio y buscando algo parecido, se logro identificar que estaba cifrado en Vigenere.
Se te da un mensaje, una clave y la tabla de letras.
se busca la letra del mensaje a la izquierda luego la letra clave arriba y donde se juntan ahi es la letra de nuestro mensaje cifrado.

Para descifrarlo.
1. buscas a la izquierda la letra de la llave, y buscas de izquierda a derecha la letra del mensaje, donde encuentres la letra, en esa columna, la letra que este asignada a esa columna en la parte de arriba, esa letra es la letra del mensaje descifrado.
2. Repetimos con cada letra.
Con CyberChef se hace directo dandole la llave.
La bandera es CRYPTOISFUN

## Notas adicionales

## Referencias
