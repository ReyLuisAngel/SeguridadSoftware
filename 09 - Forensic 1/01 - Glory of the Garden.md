## Descripción
This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.cylabacademy.net/library/0b84012e7d505751ee79c0407057962df7324463d7f8495cb79f5fb2dd998d7d/garden.jpg).

HINTS
1
What is a hex editor?
## Solución
```
descargamos el archivo y lo vismos con strings para mostrar cadenas con mas de 10 caracteres, al final aparecio la bandera.

strings -n 10 garden.jpg 
strings -n 10 garden.jpg | grep academy
con grep podriamos sacar la bandera directamente
```
academy{more_than_m33ts_the_3y36c4fc727}
## Notas adicionales

## Referencias
