## Descripción 
Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://challenge-files.cylabacademy.net/library/f7b0490c7122b66d8882c3da0c6b027eab5a9ffa3ea6b5e4c903bc3f30a950aa/flag.png).
## Solución 
```
┌──(kali㉿kali)-[~]
└─$ binwalk flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 700 x 450, 8-bit/color RGB, non-interlaced
75            0x4B            Zlib compressed data, default compression
15929         0x3E39          Zip archive data, at least v1.0 to extract, name: secret/
15994         0x3E7A          Zip archive data, at least v1.0 to extract, compressed size: 5517, uncompressed size: 5517, name: secret/flag.png
21746         0x54F2          End of Zip archive, footer length: 22

                                                                                     
┌──(kali㉿kali)-[~]
└─$ binwalk -e flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
75            0x4B            Zlib compressed data, default compression
15929         0x3E39          Zip archive data, at least v1.0 to extract, name: secret/
15994         0x3E7A          Zip archive data, at least v1.0 to extract, compressed size: 5517, uncompressed size: 5517, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                                     
┌──(kali㉿kali)-[~]
└─$ cd _flag.png.extracted/secret/
ls -la
total 16
drwxr-xr-x 2 kali kali 4096 Sep 23 00:33 .
drwxrwxr-x 3 kali kali 4096 Oct 17 23:04 ..
-rw-r--r-- 1 kali kali 5517 Sep 23 00:33 flag.png
                                                                                     
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ python3 -m http.server 8080
Serving HTTP on 0.0.0.0 port 8080 (http://0.0.0.0:8080/) ...
```
## Notas adicionales 
* Herramientas como `binwalk` o `foremost` escanean todo el archivo binario buscando las firmas hexadecimales de estos formatos ocultos (como `PK\x03\x04` para un ZIP) y los extraen cortando el archivo desde ese punto
## Referencias