## Descripción 
We found this [packet capture](https://challenge-files.cylabacademy.net/library/e64f2c2aaf9bf531af7be1787c1407c47a4cc7b57f251d5108a1151e9721a2d6/shark-on-wire-1-capture.pcap). Recover the flag.
## Solución 
```
Son69-academy@webshell:~$ wget https://challenge-files.cylabacademy.net/library/e64f2c2aaf9bf531af7be1787c1407c47a4cc7b57f251d5108a1151e9721a2d6/shark-on-wire-1-capture.pcap
--2026-09-28 17:04:18--  https://challenge-files.cylabacademy.net/library/e64f2c2aaf9bf531af7be1787c1407c47a4cc7b57f251d5108a1151e9721a2d6/shark-on-wire-1-capture.pcap
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 3.160.5.95, 3.160.5.40, 3.160.5.64, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 239455 (234K) [application/octet-stream]
Saving to: 'shark-on-wire-1-capture.pcap.1'

shark-on-wire-1-capt 100%[===================>] 233.84K  --.-KB/s    in 0.1s    

2026-09-28 17:04:18 (1.85 MB/s) - 'shark-on-wire-1-capture.pcap.1' saved [239455/239455]
Son69-academy@webshell:~$ file shark-on-wire-1-capture.pcap.1
shark-on-wire-1-capture.pcap.1: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
Son69-academy@webshell:~$ tshark -r shark-on-wire-1-capture.pcap.1 -Y "udp.stream eq 6" -T fields -e data | xxd -r -p
academy{StaT31355_636f6e6e}
```

## Notas adicionales 
* Se descargó el archivo PCAP proporcionado por el reto y se analizó el tráfico de red mediante `tshark`. Se filtraron los paquetes UDP y se identificaron los diferentes UDP streams. Posteriormente se revisó el contenido de los streams hasta localizar aquel que contenía la información de la bandera. La pista del reto indicaba utilizar Wireshark y seguir los streams para reconstruir la comunicación.
## Referencias
* https://webshell.cylabacademy.org/