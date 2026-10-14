## Descripción 
Fix the syntax error in this Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución 
```
wget https://artifacts.picoctf.net/c/25/fixme1.py
--2026-08-26 16:37:07--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                       100%[=======================================================>]     837  --.-KB/s    in 0s      

2026-08-26 16:37:07 (271 MB/s) - 'fixme1.py' saved [837/837]

python fixme1.py
  File "/home/Son69-academy/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent

nano -l fixme1.py
 
python fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```
## Notas adicionales 
* Los scripts o programas en python pueden no ejecutarse correctamente debido a errores de sintaxis, se corrigen y listo
* nano -l - abre el archivo en el editor y muestra los números de linea 
## Referencias
* https://webshell.cylabacademy.org/