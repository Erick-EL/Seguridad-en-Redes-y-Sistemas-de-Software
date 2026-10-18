## Descripción 
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.

To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!

Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.cylabacademy.net/library/88815ae7a4641c35f494d4d4b56e618428fe5cfb6a8b47c7a600eb98d670a72b/myNetworkTraffic.pcap) and try to get the flag.
## Solución 
```
Las últimas 7 subcadenas inyectadas forman el mensaje final:

1. `YWNhZGVteQ==` ➔ `academy`
    
2. `ezF0X3c0cw==` ➔ `{1t_w4s`
    
3. `bnRfdGg0dA==` ➔ `nt_th4t`
    
4. `XzM0c3lfdA==` ➔ `_34sy_t`
    
5. `YmhfNHJfZA==` ➔ `bh_4r_d`
    
6. `ZDIwNzVmMA==` ➔ `d2075f0`
    
7. `fQ==` ➔ `}`
    

Al unir las partes decodificadas se obtiene la bandera: **`academy{1t_w4snt_th4t_34sy_tbh_4r_dd2075f0}`**
```
## Notas adicionales 
- **Epoch Time (`frame.time_epoch`):** Es el tiempo en segundos (y microsegundos) transcurrido desde el 1 de enero de 1970. A diferencia de `frame.time_relative` (que es el que muestran Wireshark/tshark por defecto), el Epoch Time es absoluto e inmutable, convirtiéndolo en la herramienta perfecta para ordenar reconstrucciones forenses manipuladas.
- **TCP SYN Payload:** Inyectar datos en paquetes `[SYN]` es una técnica de _Covert Channel_ muy efectiva para evadir firewalls antiguos, ya que muchos sistemas de detección de intrusos (IDS) asumen que los paquetes SYN solo sirven para el _Handshake_ (saludo de 3 vías) y no inspeccionan su cuerpo en busca de firmas maliciosas
## Referencias
* gemini