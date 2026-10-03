## Descripción 
Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.
## Solución 
```
```
tshark -r shark-on-wire-2-capture.pcap \
-T fields -e udp.srcport \
"udp and udp.dstport == 22" |
grep -v 5000 |
awk '{printf "%c", ($1 - 5000)}'
```

Finalmente se obtuvo la bandera:

```
academy{p1LLf3r3d_data_v1a_st3g0}
## Notas adicionales 
- Se utilizó `tshark` para analizar la captura sin necesidad de abrir Wireshark.
- La información no estaba almacenada directamente como texto en los paquetes.
- Los caracteres estaban codificados mediante los **puertos de origen UDP**.
- El valor `5000` se utilizó como base para obtener los códigos ASCII.
- Restando `5000` de cada puerto se obtuvieron los valores ASCII correspondientes a los caracteres de la bandera.
- Este reto es un ejemplo de ocultamiento de información dentro de datos de una comunicación de red.
## Referencias
* ChatGPT