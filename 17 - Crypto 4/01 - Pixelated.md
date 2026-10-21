## Descripción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.cylabacademy.net/library/fa686cfe375627b0131e670a19ec4775a873562ee3006dae8a40796e3e2b5e3c/scrambled1.png) [scrambled2.png](https://challenge-files.cylabacademy.net/library/fa686cfe375627b0131e670a19ec4775a873562ee3006dae8a40796e3e2b5e3c/scrambled2.png)
Hints
1
[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
2
Think of different ways you can "stack" images
## Solución
```
academy{2f16d0c4}
```
El profe procede a realizar varias pruebas con las imagenes ya descargadas.
Investigamos en las pistas y vamos al link para comprender la criptografía visual.
Vemos que una de las tecnicas es separar por pixeles ósea tener dos imagenes que si se sobrepone una encima de otra aparece la información que buscamos.
El profe vio que cambiando el nombre de la imagen y creando un script se podrian juntar.
1. Con la IA creamos un script que juntaba las dos imagenes y nos daba una imagen resultante.
2. Ahora con python 3 lo corremos y despues de obtener el archivo lo pasamos a base64. base64 bandera.png
3. Con ayuda de un decodificador o ciberchef observamos la imagen y su contenido obteniendo asi la bandera.
## Notas adicionales

## Referencias
