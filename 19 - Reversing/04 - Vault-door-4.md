## Descripción
his vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://challenge-files.cylabacademy.net/library/59daf48711652c50a1e865dec9f451606471c2dd0ec3b699a5e3ee2b73cc446d/VaultDoor4.java) 
Hints
1
Use a search engine to find an "ASCII table"
2
You will also need to know the difference between octal, decimal, and hexadecimal numbers.
## Solución
```
academy{jU5t_4_bUnCh_0f_bYt3s_6a8a9e96bc}
```
Para resolver este reto, necesitamos analizar el arreglo `myBytes` dentro del archivo `VaultDoor4.java`. El programa verifica la contraseña comparando los caracteres ingresados contra este arreglo, el cual oculta la contraseña dividiéndola en cuatro partes codificadas en diferentes bases numéricas.

Aquí tienes los pasos exactos para decodificar cada sección usando una tabla ASCII:

- **Paso 1: Decimales.** Los primeros ocho valores (106, 85, 53, 116, 95, 52, 95, 98) están en formato decimal. Al buscarlos en una tabla ASCII, obtenemos la cadena `jU5t_4_b`.
    
- **Paso 2: Hexadecimales.** Los siguientes ocho valores (0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f) están en formato hexadecimal. Su conversión a texto es `UnCh_0f_`.
    
- **Paso 3: Octales.** Los valores de la tercera fila (0142, 0131, 0164, 063, 0163, 0137, 066, 0141) están en formato octal, lo cual se identifica por el cero al inicio. Al convertirlos a texto, se descifra como `bYt3s_6a`.
    
- **Paso 4: Caracteres directos.** La última fila simplemente contiene los caracteres literales envueltos en comillas simples ('8', 'a', '9', 'e', '9', '6', 'b', 'c'). Juntos forman `8a9e96bc`.
    

Al unir todas las partes secuencialmente, obtenemos la contraseña completa. Basado en el método `main` del código fuente, el programa recorta la entrada asumiendo que está envuelta en el prefijo `academy{`.

Por lo tanto, tu bandera correcta para enviar en la plataforma es:**`academy{jU5t_4_bUnCh_0f_bYt3s_6a8a9e96bc}`**
## Notas adicionales

## Referencias
