## Descripción 
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución 
```
wget https://artifacts.picoctf.net/c/14/level2.py

wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc

Son69-academy@webshell:~$ python level2.py
Please enter correct password for flag: yi
That password is incorrect
Son69-academy@webshell:~$ nano -l level2.py
Son69-academy@webshell:~$ python level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}

>>> en otra terminal con python convertimos el password: 
python
Python 3.12.4 (tags/v3.12.4:8e8a4ba, Jun  6 2024, 19:30:16) [MSC v.1940 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39)
'4ec9'
```
## Notas adicionales 
* se abre el archivo con editor de texto y se obtiene la contraseña convirtiéndola en otro cmd extra con python en el 
## Referencias
* https://webshell.cylabacademy.org/
* cmd extra 