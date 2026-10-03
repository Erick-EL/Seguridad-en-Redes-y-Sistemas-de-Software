## Descripción 
What does this bDNhcm5fdGgzX3IwcDM1 mean? I think it has something to do with bases.
## Solución 
```>>> import base64
>>> base64.b64decode("bDNhcm5fdGgzX3IwcDM1")
b'l3arn_th3_r0p35'
```
picoCTF{l3arn_th3_r0p35}
## Notas adicionales 
*  Primero se tiene que hacer el import para despues poder usarlo en python
## Referencias
* https://webshell.cylabacademy.org/