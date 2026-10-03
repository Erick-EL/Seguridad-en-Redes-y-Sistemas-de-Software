## Descripción 
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?
## Solución 
```Son69-academy@webshell:~$ nc fickle-tempest.picoctf.net 59250 | grep pico
picoCTF{digital_plumb3r_A01Bc3eC}
```
picoCTF{digital_plumb3r_A01Bc3eC}
## Notas adicionales 
 *  Se tiene que obtener el archivo de forma que ya sea que lo guardes para obtener la bandera o que directamente al puerto apliques un grep para obtenerla de esta otra forma, ambas son funcionales y la barra vertical llamada "pipe ( | )" redirige la salida de un comando a otro comando
## Referencias
* https://webshell.cylabacademy.org/