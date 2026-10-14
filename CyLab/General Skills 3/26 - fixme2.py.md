## Descripción 
Fix the syntax error in the Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
## Solución 
```
wget https://artifacts.picoctf.net/c/4/fixme2.py
--2026-08-26 16:44:57--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.40, 3.160.5.18, 3.160.5.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                       100%[=======================================================>]   1.00K  --.-KB/s    in 0s      

2026-08-26 16:44:57 (24.4 MB/s) - 'fixme2.py' saved [1029/1029]

python fixme2.py
  File "/home/Son69-academy/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?

>> hay que corregir el error 

Son69-academy@webshell:~$ nano -l fixme2.py
Son69-academy@webshell:~$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
```
## Notas adicionales 
* Los scripts o programas en python pueden no ejecutarse correctamente debido a errores de sintaxis, se corrigen y listo
* nano -l - abre el archivo en el editor y muestra los números de linea 
## Referencias
* cmd extra 
* https://webshell.cylabacademy.org/