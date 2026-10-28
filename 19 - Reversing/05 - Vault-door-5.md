## Descripción
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://challenge-files.cylabacademy.net/library/e4963169ad8e63b55d19fbf55ec800339ef0aa77274fdf2f1bdb7632246d514d/VaultDoor5.java) 
Hints
1
You may find an encoder/decoder tool helpful, such as [https://encoding.tools/](https://encoding.tools/)
2
Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.
## Solución
```
academy{c0nv3rt1ng_fr0m_ba5e_64_953e9301}
```
El código en `VaultDoor5.java` oculta la contraseña aplicando dos capas de codificación a la entrada del usuario: primero la convierte a formato URL mediante el método `urlEncode` y luego le aplica Base64 con el método `base64Encode`. Para obtener la contraseña original, debemos realizar el proceso inverso sobre la cadena de texto `expected`.

**Paso 1: Decodificar Base64** Tomamos la cadena codificada completa (`JTYzJTMw...`) del código fuente. Al decodificarla desde Base64, obtenemos una secuencia de caracteres en formato URL: `%63%30%6e%76%33%72%74%31%6e%67%5f%66%72%30%6d%5f%62%61%35%65%5f%36%34%5f%39%35%33%65%39%33%30%31`

**Paso 2: Decodificar URL** El formato URL utiliza el símbolo `%` seguido de valores hexadecimales para representar texto. Al traducir estos valores a sus correspondientes caracteres ASCII (por ejemplo, `%63` es `c`, `%30` es `0`), el texto plano resultante es:`c0nv3rt1ng_fr0m_ba5e_64_953e9301`

**Bandera Final** Siguiendo la estructura exigida por el método `main` para validar el acceso, la bandera completa es: **`academy{c0nv3rt1ng_fr0m_ba5e_64_953e9301}`**
## Notas adicionales

## Referencias
