## Descripción 
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg)
## Solución 
```
Son69-academy@webshell:~$ exiftool cat.jpg 
ExifTool Version Number         : 12.40
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2026:09:23 02:44:41+00:00
File Access Date/Time           : 2026:10:18 02:29:36+00:00
File Inode Change Date/Time     : 2026:10:18 02:29:36+00:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 13.25
License                         : YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
Son69-academy@webshell:~$ echo "YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
academy{the_m3tadata_1s_modified}
```
## Notas adicionales 
* **Metadatos EXIF:** Son etiquetas incrustadas en archivos gráficos (JPEG, TIFF) y de audio que describen propiedades técnicas. En seguridad defensiva y privacidad (OSINT), es una práctica habitual limpiar o eliminar estos metadatos (_scrubbing_) antes de publicar imágenes en la web para evitar fugas de información sensible (como coordenadas GPS o identificadores de dispositivos)
## Referencias
