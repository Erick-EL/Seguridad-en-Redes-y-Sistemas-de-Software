## Descripción 
There's an interesting script in the user's home directory

The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

`Hostname: saturn.picoctf.net Port: 62310 Username: picoplayer Password: password`
## Solución 
```
ssh picoplayer@saturn.picoctf.net -p 62310 
ssh picoplayer@saturn.picoctf.net -p 62310 
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 6.17.0-1019-aws x86_64)

picoplayer@challenge:~$ ./useless
Read the code first
picoplayer@challenge:~$ cat useless

        else
          echo "Read the manual"
         
        fi
fi
picoplayer@challenge:~$ man useless

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_8504}
     
     exit
```
## Notas adicionales 
* man - me proporciona un manual de ayuda completo de un comando o ejecutable si es que la hay
## Referencias
* https://webshell.cylabacademy.org/