## Descripción 
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.cylabacademy.net/library/34106bdd624e0aec8af0ba0e9c52e7fd45d5d1415761ffc98b2130cace440057/dds1-alpine.flag.img.gz)
Have you ever used `file` to determine what a file was?
Relevant terminal-fu in Challenge Library: [https://learn.cylabacademy.org/library/85](https://learn.cylabacademy.org/library/85)
## Solución 
```
└─$ gunzip dds1-alpine.flag.img.gz 
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ ls      
concat_v.png  dds1-alpine.flag.img  moonwalk       WebNet0
corrupt       like1000              tunn3l_v1s10n  whitepages
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ strings -n 10  dds1-alpine.flag.img | grep academy
  SAY academy{f0r3ns1c4t0r_n30phyt3_6502313d}

```
## Notas adicionales 
* gunzip funciona para descomprimir los archivos con terminación .gz
## Referencias