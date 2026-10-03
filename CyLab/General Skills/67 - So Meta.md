## Descripción 
Find the flag in this [picture](https://challenge-files.cylabacademy.net/library/a3bb49a714b2015cbba62c5a2db7238a40609a2fbbd7fbe21af7a8f5068cc7b8/pico_img.png).
## Solución 
```
Son69-academy@webshell:~$ wget https://challenge-files.cylabacademy.net/library/a3bb49a714b2015cbba62c5a2db7238a40609a2fbbd7fbe21af7a8f5068cc7b8/pico_img.png
--2026-09-28 16:44:44--  https://challenge-files.cylabacademy.net/library/a3bb49a714b2015cbba62c5a2db7238a40609a2fbbd7fbe21af7a8f5068cc7b8/pico_img.png
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 3.160.5.18, 3.160.5.95, 3.160.5.64, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108795 (106K) [application/octet-stream]
Saving to: 'pico_img.png'

pico_img.png                                               100%[========================================================================================================================================>] 106.25K  --.-KB/s    in 0.05s   

2026-09-28 16:44:44 (1.93 MB/s) - 'pico_img.png' saved [108795/108795]

Son69-academy@webshell:~$ strings -n 10 pico_img.png 
```
## Notas adicionales 
* Con strings -n 10 indicas que quires obtener hasta los primeros 10 caracteres que se encuentran en la imagen 
## Referencias
* https://webshell.cylabacademy.org/