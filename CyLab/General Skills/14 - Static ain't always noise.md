## Descripción 
Can you look at the data in this binary? The bash script might help!
## Solución 
```
wget https://challenge-files.picoctf.net/c_wily_courier/34dfb62cf2c94a618c7cdc292ff1c4062b104773695071e9a16ab25ad8cc935c/static
wget https://challenge-files.picoctf.net/c_wily_courier/34dfb62cf2c94a618c7cdc292ff1c4062b104773695071e9a16ab25ad8cc935c/ltdis.sh
:~$ chmod +x ltdis.sh
:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_20335e41}
```
## Notas adicionales 
* sh son archivos que contienen comandos de linux agrupados, se les llama scripts de bash 
* rm 
## Referencias
* https://webshell.cylabacademy.org/