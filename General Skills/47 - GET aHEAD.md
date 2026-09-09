## Descripción 
Find the flag being held on this server to get ahead of the competition

http://wily-courier.picoctf.net:62526/
## Solución 
```
curl -s -I http://wily-courier.picoctf.net:62526/
HTTP/1.1 200 OK
Date: Mon, 07 Sep 2026 16:29:36 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8
```
## Notas adicionales 
* curl -s -i - realiza una petición HTTP de tipo **HEAD** a un servidor web para obtener únicamente sus **cabeceras de respuesta**, de forma completamente **silenciosa** (sin mostrar barras de progreso ni mensajes de error)
## Referencias
* Terminal de Kali 