## Descripción 
Our flag printing service has started glitching!
## Solución 
```Son69-academy@webshell:~$ nc saturn.picoctf.net 60457
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
^C
Son69-academy@webshell:~$ python
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
'picoCTF{gl17ch_m3_n07_a4392d2e}'
```
picoCTF{gl17ch_m3_n07_a4392d2e}
## Notas adicionales 
 *  python utilixxs el + para concatenar cadenas 
 * chr() es una funcion de python que convierte un numero a su correspondiente carácter ASCII
 * Esto fue simplemente suma de cadenas y caracteres
## Referencias
* https://webshell.cylabacademy.org/