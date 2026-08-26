## Descripción 
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.

There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución 
```
wget https://artifacts.picoctf.net/c/18/level3.py

wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc

wget https://artifacts.picoctf.net/c/18/level3.hash.bin

Son69-academy@webshell:~$ tail level3.py



level_3_pw_check()


# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
Son69-academy@webshell:~$ python level3.py
Please enter correct password for flag: 8799
That password is incorrect
Son69-academy@webshell:~$ python level3.py
Please enter correct password for flag: d3ab
That password is incorrect
Son69-academy@webshell:~$ python level3.py
Please enter correct password for flag: 6f3d
That password is incorrect
Son69-academy@webshell:~$ python level3.py
Please enter correct password for flag: 1ea2
That password is incorrect
Son69-academy@webshell:~$ python level3.py
Please enter correct password for flag: acaf
That password is incorrect
Son69-academy@webshell:~$ python level3.py
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f} 
```
## Notas adicionales 
* el mismo archivo te indica que las contraseñas están al final del archivo 
* se obtienen usando "tail" para que te de el final del archivo y solo toca probar con todas las contraseñas
## Referencias
* https://webshell.cylabacademy.org/
* cmd extra 