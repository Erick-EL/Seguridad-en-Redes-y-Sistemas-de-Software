## Descripción 
Run the Python script and convert the given number from decimal to binary to get the flag.

[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)
## Solución 
```
wget https://artifacts.picoctf.net/c/24/convertme.py
--2026-08-26 16:30:19--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.64, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                    100%[=======================================================>]   1.16K  --.-KB/s    in 0s      

2026-08-26 16:30:19 (40.5 MB/s) - 'convertme.py' saved [1189/1189]

:~$ python convertme.py
If 23 is in decimal base, what is it in binary base?
Answer: 0b10111
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}

>>> en otra terminal hacemos la conversion:

>python
Python 3.12.4 (tags/v3.12.4:8e8a4ba, Jun  6 2024, 19:30:16) [MSC v.1940 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> bin(23)
'0b10111'
```
## Notas adicionales 
*  Se abre otra terminal externa para poder ingresar en ella a python y hacer la conversión sin problemas 
## Referencias
*  https://webshell.cylabacademy.org/