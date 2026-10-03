## Descripción 
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/77/challenge.zip)
Version control can help you recover files if you change or lose them!
## Solución 
```
wget https://artifacts.picoctf.net/c_titan/77/challenge.zip
unzip challenge.zip 
on69-academy@webshell:~$ cd drop-in
Son69-academy@webshell:~/drop-in$ git log
Son69-academy@webshell:~/drop-in$ git checkout 3d5ec8a26ee7b092a1760fea18f384c35e435139
HEAD is now at 3d5ec8a create flag
Son69-academy@webshell:~/drop-in$ ls
exit  message.txt
Son69-academy@webshell:~/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_30e86d36}
Son69-academy@webshell:~/dro
```
## Notas adicionales 
* git log - sirve para ver el registro de las acciones realizadas por el administrador 
* git checkout - es para devolver el estado anterior hasta el punto exacto que se le de 
## Referencias
* https://webshell.cylabacademy.org/