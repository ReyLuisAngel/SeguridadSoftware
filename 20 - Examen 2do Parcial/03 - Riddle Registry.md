## Descripción
Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered. Find the PDF file here [Hidden Confidential Document](https://challenge-files.cylabacademy.net/library/f1a59c8fe4c030bdcdce963b06148196c62afa61f1e959134cd5b547347fddaf/confidential.pdf) and uncover the flag within the metadata.

Hints
1
Don't be fooled by the visible text; it’s just a decoy!
2
Look beyond the surface for hidden clues
## Solución
```

```
**1. Usar ExifTool (Recomendado)** Ejecuta el siguiente comando para revelar toda la información oculta del archivo: 
`exiftool confidential.pdf` 
Revisa la lista de resultados. La bandera suele estar guardada en campos como "Title", "Author".
```
ExifTool Version Number         : 12.40
File Name                       : confidential.pdf
Directory                       : .
File Size                       : 178 KiB
File Modification Date/Time     : 2026:09:23 06:28:06+00:00
File Access Date/Time           : 2026:10:28 00:15:39+00:00
File Inode Change Date/Time     : 2026:10:28 00:15:39+00:00
File Permissions                : -rw-rw-r--
File Type                       : PDF
File Type Extension             : pdf
MIME Type                       : application/pdf
PDF Version                     : 1.7
Linearized                      : No
Page Count                      : 1
Producer                        : PyPDF2
Author                          : YWNhZGVteXtwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV8zY2M3Y2VhOX0=
```
El author esta codificado en base 64, ahi se encuentra nuestra bandera.
2.Decodificar la bandera que se encuentra en base64
## Notas adicionales

## Referencias
