## Descripción 
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?

Download the suspicious file [here](https://challenge-files.cylabacademy.net/library/648efad3a02ebcd4c6fa34acb864030945055931c435b53f28821b672500ad3c/flag2of2-final.pdf).
## Solución 
```
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ binwalk flag2of2-final.pdf 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 200 x 40, 4-bit colormap, non-interlaced
453           0x1C5           PDF document, version: "1.4"
688           0x2B0           Zlib compressed data, default compression

                                                                                                                    
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ pdftotext flag2of2-final.pdf 
                                                                                                                    
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ pdftotext flag2of2-final.pdf - 
1n_pn9_&_pdf_07226ac4}


                                                                                                                    
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ mv flag2of2-final.pdf imagen.png
                                                                                                                    
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ tesseract imagen.png stdout
academy(f1u3n7_

academy(f1u3n7_1n_pn9_&_pdf_07226ac4}
```
## Notas adicionales 
* Siempre usa `binwalk`, `exiftool` o `strings` cuando un archivo parezca comportarse de forma anómala para entender exactamente qué flujos de datos contiene
## Referencias