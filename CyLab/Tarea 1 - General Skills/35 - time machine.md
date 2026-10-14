	## Descripción 
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/163/challenge.zip)
## Solución 
```
wget https://artifacts.picoctf.net/c_titan/163/challenge.zip
--2026-08-30 04:46:59--  https://artifacts.picoctf.net/c_titan/163/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17741 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[========================================================================================================================================>]  17.33K  --.-KB/s    in 0.001s  

2026-08-30 04:46:59 (20.2 MB/s) - 'challenge.zip' saved [17741/17741]

Son69-academy@webshell:~$ unzip challenge.zip 
Son69-academy@webshell:~$ cd drop-in/
Son69-academy@webshell:~/drop-in$ git log
commit e65fedb3a72a16c577f4b17023b63997134b307d (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:29 2024 +0000

    picoCTF{t1m3m@ch1n3_88c35e3b}
(END)
```
## Notas adicionales 
* git log - sirve para ver el registro de las acciones realizadas por el administrador 
## Referencias
*  https://webshell.cylabacademy.org/