## Descripción 
This website can be rendered only by picobrowser, go and catch the flag!

[http://fickle-tempest.picoctf.net:56386](http://fickle-tempest.picoctf.net:56386)
You don't need to download a new web browser
## Solución 
```
</html>Son69-academy@webshell:~$ curl -s http://fickle-tempest.picoctf.net:56386/flag -H "User-Agent: picobrowser" | grep pico
         <!-- <strong>Title</strong> --> picobrowser!
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}</code></p>
```
picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
## Notas adicionales 
* Curl - El comando funciona engañando al servidor web mediante la **falsificación del User-Agent** (User-Agent Spoofing)
## Referencias
* http://fickle-tempest.picoctf.net:56386/flag
* https://webshell.cylabacademy.org/