## Descripción 
This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.cylabacademy.net/library/3c60c5a7f7a8067606c51d4b4b3c7913fae709b11e2f2c7adbc0a0b4cda452ff/garden.jpg).
What is a hex editor?
## Solución 
```
Son69-academy@webshell:~$ wget https://challenge-files.cylabacademy.net/library/3c60c5a7f7a8067606c51d4b4b3c7913fae709b11e2f2c7adbc0a0b4cda452ff/garden.jpg
--2026-09-28 16:36:30--  https://challenge-files.cylabacademy.net/library/3c60c5a7f7a8067606c51d4b4b3c7913fae709b11e2f2c7adbc0a0b4cda452ff/garden.jpg
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 3.160.5.18, 3.160.5.95, 3.160.5.64, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295191 (2.2M) [application/octet-stream]
Saving to: 'garden.jpg'

garden.jpg           100%[===================>]   2.19M  1.83MB/s    in 1.2s    

2026-09-28 16:36:31 (1.83 MB/s) - 'garden.jpg' saved [2295191/2295191]

Son69-academy@webshell:~$ strings -n 10 garden.jpg
```
academy{more_than_m33ts_the_3y3ff3b9e86}
## Notas adicionales 
* Con strings -n 10 indicas que quires obtener hasta los primeros 10 caracteres que se encuentran en la imagen 
## Referencias
* https://webshell.cylabacademy.org/