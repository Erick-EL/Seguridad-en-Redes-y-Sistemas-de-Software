## Descripción 
Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/162bc8bf6dd1abbc5269c16570e170277369a39cf46bdd8d99443e136fabcc5f/disk.flag.img.gz)
## Solución 
```
┌──(kali㉿kali)-[~/cylab]
└─$ mmls disk.flag.img            
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ fls -o 360448 -r disk.flag.img 1995  
r/r 2363:       .ash_history
d/d 3981:       my_folder
+ r/r * 2082(realloc):  flag.txt
+ r/r 2371:     flag.uni.txt
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ fls -o 360448 -r disk.flag.img 2371
Error extracting file from image (ext2fs_dir_open_meta: Error reading directory contents: 2371
)
                                                                                     
┌──(kali㉿kali)-[~/cylab]
└─$ icat -o 360448 -r disk.flag.img 2371
academy{by73_5urf3r_85e9b307}

```
## Notas adicionales 
*  se uso el icat y el fls `fls` lee la estructura del sistema de archivos sin montarlo, permitiendo ver inodos de archivos eliminados.
## Referencias
