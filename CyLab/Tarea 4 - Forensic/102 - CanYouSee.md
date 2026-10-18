## Descripción 
How about some hide and seek?

Download this file [here](https://challenge-files.cylabacademy.net/library/3781b74e6ee2cd04bb03da6614e1c184422f725bf14a19d5b61f8b2038e1c11c/unknown.zip).
## Solución 
```
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ unzip unknown.zip  
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
                                                                                                                    
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 13.55
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2026:09:23 01:17:45-04:00
File Access Date/Time           : 2026:10:17 23:32:57-04:00
File Inode Change Date/Time     : 2026:10:17 23:32:57-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 12.76
Attribution URL                 : YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fOTI2NmRlMWV9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
                                                                                                                    
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ echo "YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fOTI2NmRlMWV9Cg==" | base64 -d
academy{ME74D47A_HIDD3N_9266de1e}

```
## Notas adicionales 
* Revisar los metadatos de un archivo multimedia siempre debe ser tu paso número 1 en cualquier reto de la categoría Forensics. Como buena práctica en Kali, puedes crear un hábito ejecutando `exiftool archivo` y `strings archivo | head -n 20` apenas descargas la evidencia
## Referencias