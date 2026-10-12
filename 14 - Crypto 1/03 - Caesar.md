## Descripción
Decrypt this message. Message: [message](https://challenge-files.cylabacademy.net/library/eb4325fac37933de66857090e6c78c226267394ccaf5c079ff593e3e33b4b95a/data.enc) 
Hints
1
Caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)
## Solución
```
academy{crossingtherubiconulqcojpd}
```
Buscamos como funcionaba el cifrado Caesar y con ello desciframos el mensaje oculto.
Utilizamos cyberchef para descifrarlo y la bandera apareció sola.
Movemos el desplazamiento hasta que salga algo legible.
# 2
Una segunda solución podría ser usar python para descifrarlo.
## Notas adicionales
El cifrado de Caesar es recorrer 3 posiciones a la derecha en el abecedario dicha letra, por lo que para descifrarlo solo recorremos 3 letras a la izquierda cada letra que se nos dio.
## Referencias
