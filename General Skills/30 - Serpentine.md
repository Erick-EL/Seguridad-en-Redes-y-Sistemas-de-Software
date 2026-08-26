## Descripción 
Find the flag in the Python script!

[Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
## Solución 
```
wget https://artifacts.picoctf.net/c/35/serpentine.py

Son69-academy@webshell:~$ python serpentine.py 
Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) x

I did not understand "x", input only "a", "b" or "c"


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
Son69-academy@webshell:~$ nano serpentine.py 
Son69-academy@webshell:~$ nano serpentine.py 
Son69-academy@webshell:~$ python serpentine.py 

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
```
## Notas adicionales 
* Se tiene que revisar la logica del archivo y revisar el porque se generan los errores como en este caso el error era que no se mandaba a llamar a la función 
## Referencias
* https://webshell.cylabacademy.org/