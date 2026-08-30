## Descripción 
Someone's commits seems to be preventing the program from working. Who is it?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/159/challenge.zip)
## Solución 
```
wget https://artifacts.picoctf.net/c_titan/159/challenge.zip
--2026-08-30 04:51:18--  https://artifacts.picoctf.net/c_titan/159/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 293915 (287K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[========================================================================================================================================>] 287.03K  1.84MB/s    in 0.2s    

2026-08-30 04:51:18 (1.84 MB/s) - 'challenge.zip' saved [293915/293915]

Son69-academy@webshell:~$ unzip challenge.zip 
Son69-academy@webshell:~$ cd drop-in/
Son69-academy@webshell:~/drop-in$ ls
message.py
Son69-academy@webshell:~/drop-in$ git blame message.py
23e9d4ce (picoCTF{@sk_th3_1nt3rn_81e716ff} 2024-03-12 00:07:15 +0000 1) print("Hello, World!"
```
## Notas adicionales 
* git blame - Imprime en pantalla cada línea del archivo y, a la izquierda, te muestra el _hash_ del commit y el **nombre de la persona** que escribió esa línea específica
## Referencias
* El buen google 
*  https://webshell.cylabacademy.org/