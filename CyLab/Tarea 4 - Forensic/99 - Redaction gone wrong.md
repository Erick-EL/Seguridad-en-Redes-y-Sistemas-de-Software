## Descripción 
Now you DON’T see me. This [report](https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a27705e2c94103/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Solución 
```
┌──(kali㉿kali)-[~]
└─$ pdftotext Financial_Report_for_ABC_Labs.pdf - | grep -i "academy"
academy{C4n_Y0u_S33_m3_fully}

```
## Notas adicionales 
* Herramientas como `pdfdetach`, `pdfinfo` y `peepdf` son excelentes para complementar el análisis forense de archivos PDF sospechosos o maliciosos, permitiendo extraer archivos adjuntos, JavaScript incrustado o metadatos ocultos
## Referencias