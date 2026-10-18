## Descripción 
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?

You can download the challenge files here:

- [challenge.zip](https://challenge-files.cylabacademy.net/library/dd59b9740e3ce6a2a25dd2e5eebb59d3d6734cbaef0d41e03b42af73855a97da/challenge.zip) The same files are accessible via SSH here:

`ssh -p 40858 ctf-player@xebec.cylabacademy.net`

Using the password `8d1db23b`. Accept the fingerprint with `yes`; the QR code prints as soon as you connect, and `ls` will show the same image as `flag.png`. Remember, in a shell, passwords are hidden!
## Solución 
```
┌──(kali㉿kali)-[~/_flag.png.extracted/secret]
└─$ ssh -p 40858 ctf-player@xebec.cylabacademy.net
The authenticity of host '[xebec.cylabacademy.net]:40858 ([77.113.98.131]:40858)' can't be established.
ED25519 key fingerprint is: SHA256:pXZJJueHk/xqC/LPp14k8Mb1vT0LHQpM4b9yfyz7M24
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[xebec.cylabacademy.net]:40858' (ED25519) to the list of known hosts.
ctf-player@xebec.cylabacademy.net's password: 
Permission denied, please try again.
ctf-player@xebec.cylabacademy.net's password:    
ctf-player@challenge:~/drop-in$ Connection to xebec.cylabacademy.net closed by remote host.
Connection to xebec.cylabacademy.net closed.  
```
## Notas adicionales 
* un reto que se resuelve ingresando y al momento de hacerlo aparece un código QR que simplemente se escanea 
## Referencias
* 