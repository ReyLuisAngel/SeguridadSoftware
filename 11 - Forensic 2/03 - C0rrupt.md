## Descripción
We found this [file](https://challenge-files.cylabacademy.net/library/8388ecc430588d15064755583476bec46e23d42a6d8de6e8995c19e40f2e4c58/c0rrupt-mystery). Recover the flag.

HINTS
1
Try fixing the file header
## Solución
```
Volvimos a darle a la IA el desafio
El archivo `c0rrupt-mystery` es una imagen PNG a la que le han modificado intencionalmente los bytes estructurales (su código hexadecimal) para que ningún visor de imágenes pueda abrirla.

Para recuperar la imagen y leer la bandera, necesitas editar los bytes del archivo desde tu webshell y restaurar la cabecera (header) junto con los identificadores de los bloques de datos al estándar de PNG.

**1. Analiza el archivo con pngcheck** Esta herramienta de terminal es vital para este reto porque te indicará exactamente qué bloque está fallando en cada momento.

Bash

```
sudo apt install pngcheck
pngcheck -v c0rrupt-mystery
```

_(El primer error que te lanzará será que la firma del archivo es inválida)._

**2. Edita los bytes hexadecimales** Abre el archivo utilizando un editor hexadecimal por consola.

Bash

```
hexeditor c0rrupt-mystery
```

_(Usa las flechas de tu teclado para moverte, escribe los números hexadecimales correctos para reemplazar los caracteres dañados y presiona `Ctrl + X` para guardar y salir)._

**3. Restaura la estructura paso a paso** En este reto, los creadores alteraron varias etiquetas a lo largo del archivo. Repara una por una, guarda los cambios y vuelve a correr `pngcheck` hasta que deje de marcar errores:

- **Firma PNG (Magic Bytes):** Los primeros 8 bytes de todo el archivo deben ser estrictamente **`89 50 4E 47 0D 0A 1A 0A`**.
    
- **Bloque de cabecera (IHDR):** A partir del byte 12 (offset `0x0000000C`), deben estar las letras `IHDR`. Cámbialas a su valor hexadecimal correcto: **`49 48 44 52`**.
    
- **Bloque de resolución (pHYs):** Si `pngcheck` te marca un error indicando un chunk desconocido, busca en el editor hexadecimal una palabra que se parezca a `pHYs` pero que esté mal escrita (por ejemplo, alteraron el primer byte) y corrígela a **`70 48 59 73`**.
    
- **Bloques de datos (IDAT):** Lo mismo ocurre con el bloque de la imagen. Busca el identificador dañado y arréglalo para que diga `IDAT` (**`49 44 41 54`**).
    

Una vez que `pngcheck` evalúe el archivo e imprima `OK`, podrás abrir la imagen regenerada y verás la bandera escrita en ella.

```
Le pedi a la IA que interpretara la imagen y me diera la bandera, esta es el resultado
academy{c0rrupt10n_1847995}
## Notas adicionales

## Referencias
