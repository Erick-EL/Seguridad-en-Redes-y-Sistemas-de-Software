## Descripción 
This is a really weird text file. Can you find the flag? Get the flag from [TXT](https://challenge-files.cylabacademy.net/library/a5d365fedad883763fb28c78e25a1765220bef6501848c84f2a7a7adf74d83cd/flag.txt).
## Solución 
El reto proporcionaba un archivo llamado `flag.txt`, pero la extensión `.txt` era engañosa.
Primero se utilizó:
file flag.txt
El resultado indicó que el archivo realmente era una imagen PNG:
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
Después se cambió la extensión:
mv flag.txt flag.png
Se intentó buscar la bandera con `strings`, pero no apareció porque la bandera estaba representada visualmente dentro de la imagen y no almacenada como texto.
La vulnerabilidad/concepto del reto consiste en comprender que **la extensión de un archivo no determina su formato real**. El sistema puede identificar el tipo de archivo mediante su contenido y sus firmas internas (magic bytes).
La bandera de la instancia, utilizando el formato actual de CyLab, es:
academy{now_you_know_about_extensions}
## Notas adicionales 
* Usar la IA para leer texto en imágenes también puede resultar una opción bastante útil 
## Referencias
* Google IA