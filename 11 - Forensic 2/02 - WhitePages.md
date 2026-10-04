## Descripción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.cylabacademy.net/library/164023ae7e53a7b325e50a82f7cd942427fd0f38084d555c162501500fc475c3/whitepages.txt) is all blank!

HINTS
1
There is data encoded somewhere... there might be an online decoder.
## Solución
```
Le pasamos el documento y las pistas a la IA para que nos ayudara
El archivo que parece estar en blanco en realidad contiene un mensaje binario oculto mediante el uso de dos tipos diferentes de caracteres invisibles.

- El fragmento proporcionado está compuesto por espacios normales (ASCII `0x20`) y "espacios Em" más anchos (Unicode `U+2003`).
    
- Al sustituir los espacios Em por `0` y los espacios normales por `1`, se forma una cadena binaria de 8 bits que se traduce a texto plano.
    
- La decodificación de esta secuencia revela una dirección física y la bandera del reto.
  
ReyLuis-academy@webshell:~$ python3 -c '
with open("whitepages.txt", "r", encoding="utf-8") as f:
    text = f.read()

# Convertir Em Space a 0 y espacio normal a 1
binary = text.replace("\u2003", "0").replace(" ", "1")

# Agrupar en bloques de 8 bits y convertir a caracteres ASCII
resultado = "".join([chr(int(binary[i:i+8], 2)) for i in range(0, len(binary), 8) if len(binary[i:i+8]) == 8])
print(resultado)
'

academy

SEE PUBLIC RECORDS & BACKGROUND REPORT
5000 Forbes Ave, Pittsburgh, PA 15213
academy{not_all_spaces_are_created_equal_d4c2f3dcae81af992c8e86ddecdf2dd5}

```
academy{not_all_spaces_are_created_equal_d4c2f3dcae81af992c8e86ddecdf2dd5}
## Notas adicionales

## Referencias
