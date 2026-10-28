## Descripción
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://challenge-files.cylabacademy.net/library/7ba596e841da2b21be2c33dbc90a5c3597af85887f341ee538e22bb609ba873a/VaultDoor3.java) 
Hints
1
Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.
## Solución
```

```
Le pedimos a la IA psandole una captura del reto que nos ayudara y nos pidio el archivo anidado.
Para resolver este reto de ingeniería inversa, debemos analizar cómo el programa desordena la contraseña usando cuatro ciclos `for`. Al final, compara el resultado con la cadena `jU5t_a_sna_3lpm10g747_u_4_m7re49`.

Para obtener la contraseña original, hacemos la operación inversa sobre los índices de esa cadena:

1. **Caracteres 0-7:** Se mantienen igual (`jU5t_a_s`).
    
2. **Caracteres 8-15:** Se invirtieron usando `23 - i`. Al revertirlos, se obtiene `1mpl3_an`.
    
3. **Caracteres 16-31 (pares):** Fueron asignados con `46 - i`.
    
4. **Caracteres 17-31 (impares):** Se mantuvieron en su misma posición original.
    

Al reconstruir el bloque final con las dos últimas reglas, se forma `4gr4m_4_u_777e09`.

Juntando todas las partes y agregando el formato que pide el método `main`, tu bandera correcta es: **`academy{jU5t_a_s1mpl3_an4gr4m_4_u_777e09}`**
## Notas adicionales

## Referencias
