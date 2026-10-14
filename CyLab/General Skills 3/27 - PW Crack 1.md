## Descripción 
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.
## Solución 
```
wget https://artifacts.picoctf.net/c/11/level1.py
wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
nano level1.py
Son69-academy@webshell:~$ python level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```
## Notas adicionales 
* A veces hay que revisar el, código y revisar su lógica para entender de donde se puede obtener la bandera 
## Referencias
* https://webshell.cylabacademy.org/