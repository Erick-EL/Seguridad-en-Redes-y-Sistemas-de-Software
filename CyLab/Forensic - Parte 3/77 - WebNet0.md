## Descripción 
We found this [packet capture](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/webnet0-capture.pcap) and [key](https://challenge-files.cylabacademy.net/library/2d15538465c5948f0f0626d0cdd271f74363c00aa99d694730fe98331946ab88/picopico.key). Recover the flag.
## Solución 
```
┌──(kali㉿kali)-[~/cylab/WebNet0]
└─$ ssldump -r webnet0-capture.pcap -k picopico.key -d | grep academy -A 2
Cleaned 3 remaining connection(s) from connection pool
    61 67 3a 20 61 63 61 64 65 6d 79 7b 6e 6f 6e 67    ag: academy{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
--
    67 3a 20 61 63 61 64 65 6d 79 7b 6e 6f 6e 67 73    g: academy{nongshim.shrimp.crackers}..Content-Le

```
## Notas adicionales 
* Este comando sirve para desencriptar las llaves y así obtener las banderas 
## Referencias