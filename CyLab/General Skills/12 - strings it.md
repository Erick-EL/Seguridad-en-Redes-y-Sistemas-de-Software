## Descripción 
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/094a1db42d5ae681cd9e513dcbea2d997495dd3763d50c643b939923ca86e29b/strings) without running it?
## Solución 
```
wget https://challenge-files.picoctf.net/c_fickle_tempest/094a1db42d5ae681cd9e513dcbea2d997495dd3763d50c643b939923ca86e29b/strings
ls
README.txt  file  flag  strings
file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=7e75296600ba106fbad1dd18137218feed44ecd9, for GNU/Linux 3.2.0, not stripped
strings strings | grep pico
picoCTF{5tRIng5_1T_47948C73}

```
## Notas adicionales 
* se utiliza un grep pero haciendo que solo saque las puras cadenas del archivo con el grep 
* el comando strings muestra las cadenas en un archivo binario 
## Referencias
* man strings 