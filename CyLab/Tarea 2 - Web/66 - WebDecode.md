## Descripción 
Do you know how to use the web inspector? Start searching [here](http://xebec.cylabacademy.net:29174/) to find the flag
Use the web inspector on other files included by the web page.
The flag may or may not be encoded
## Solución 
```
Son69-academy@webshell:~$ curl -s http://xebec.cylabacademy.net:29174/about.html | grep -oE 'notify_true="[^"]+"' | cut -d '"' -f2 | base64 -d
academy{web_succ3ssfully_d3c0ded_e0ea179a}
```
## Notas adicionales 
* El comando utiliza una tubería (`|`) para procesar la página en varias etapas:

```bash
curl -s URL | grep -oE 'notify_true="[^"]+"' | cut -d '"' -f2 | base64 -d
```
1. **curl** descarga `about.html`.
    
2. **grep** encuentra el atributo `notify_true` dentro del código HTML.
    
3. **cut** extrae únicamente el valor contenido entre las comillas.
    
4. **base64 -d** decodifica ese valor y revela la bandera.
En resumen:

**Descargar página → localizar `notify_true` → extraer su contenido → decodificar Base64 → obtener la bandera.**
## Referencias
* https://webshell.cylabacademy.org/
* ChatGPT