## Descripción 
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/69/challenge.zip)
## Solución 
```
 wget https://artifacts.picoctf.net/c_titan/69/challenge.zip
--2026-08-30 04:54:58--  https://artifacts.picoctf.net/c_titan/69/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.64, 3.160.5.40, 3.160.5.95, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24642 (24K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[========================================================================================================================================>]  24.06K  --.-KB/s    in 0.004s  

2026-08-30 04:54:58 (5.28 MB/s) - 'challenge.zip' saved [24642/24642]

Son69-academy@webshell:~$ unzip challenge.zip 

~/drop-in$ git branch -a

[2]+  Stopped                 git branch -a
Son69-academy@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
Son69-academy@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')Son69-academy@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
Son69-academy@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')Son69-academy@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
Son69-academy@webshell:~/drop-in$ cat flag.py
print("Printing the flag...")

print("w0rk_e4b79efb}")
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_e4b79efb}
```
## Notas adicionales 
*  Se van uniendo las partes de la llave conforme se explora cada rama 
## Referencias
* https://webshell.cylabacademy.org/