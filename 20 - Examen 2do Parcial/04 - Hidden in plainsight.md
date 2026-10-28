## Descripción
The SOC team discovered a suspiciously large log file after a recent breach. When they opened it, they found an enormous block of encoded text instead of typical logs. Could there be something hidden within? Your mission is to inspect the resulting file and reveal the real purpose of it. The team is relying on your skills to uncover any concealed information within this unusual log. Download the encoded data here: [Logs Data](https://challenge-files.cylabacademy.net/library/8389f7eb8ae95fd4453f1e2d27498905b415efec5fc738bfd0983d56c09959bf/logs.txt). Be prepared—the file is large, and examining it thoroughly is crucial .

Hints
1
Use `base64` to decode the data and generate the image file.
## Solución
```
academy{h1dd3n_1n_1m4g3_45cfe9c1}
```
1 Descargar la imagen
2 Usar exiftool img.jpg
3 Al ver en los datos observamos que existe el comentario cifrado en base 64 asi que lo decodificamos con: echo "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9" | base64 -d
El resultado es steghide:cEF6endvcmQ=
que nos indica el lugar y la contraseña para acceder a el.
4 Utilizamos steghide extract -sf img.jpg
y cuando se nos pida la contraseña la ingresamos.
5 Utilizamos lo siguiente para obtener la bandera
```
echo "cEF6endvcmQ=" | base64 -d # -> pAzzword 
steghide extract -sf img.jpg -p pAzzword 
cat flag.txt

```
## Notas adicionales

## Referencias
