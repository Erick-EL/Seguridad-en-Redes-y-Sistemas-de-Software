## Descripción 
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)}
- Can grep be instructed to look at every file in a directory and its subdirectories?
## Solución 
```
wget https://artifacts.picoctf.net/c/503/big-zip-files.zip

unzip big-zip-files.zip

ls
Addadshashanammu  Addadshashanammu.zip  README.txt  big-zip-files  big-zip-files.zip  enc_flag  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
:~$ strings big-zip-files | grep pico
strings: Warning: 'big-zip-files' is a directory
:~$ cd big-zip-files    
:~/big-zip-files$ strings big-zip-files | grep pico
strings: 'big-zip-files': No such file
:~/big-zip-files$ strings big-zip-files | grep -r pico
strings: 'big-zip-files': No such file
folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
```
## Notas adicionales 
* Se descarga y se descomprime el zip 
* grep -r - se utiliza para que la búsqueda se vuelva recursiva según el nombre que le pases hasta encontrarlo en cualquiera de todos los directorios 
## Referencias
* https://webshell.cylabacademy.org/
* el buen google para saber con que complementar el grep 