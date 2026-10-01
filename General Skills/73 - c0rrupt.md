## Descripción 
Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.
## Solución 
```
Primero se descargó el archivo desde el enlace proporcionado por el reto:

```
wget 'https://challenge-files.cylabacademy.net/library/8388ecc430588d15064755583476bec46e23d42a6d8de6e8995c19e40f2e4c58/c0rrupt-mystery'
```

Después se verificó el tipo de archivo:

```
file c0rrupt-mystery
```

El archivo no era reconocido correctamente debido a que su encabezado estaba corrupto.

Se revisaron sus primeros bytes con:

```
xxd -g 1 c0rrupt-mystery | head
```

Se identificó que el archivo debía ser un **PNG**, ya que la firma correcta de un PNG es:

```
89 50 4E 47 0D 0A 1A 0A
```

Se creó una copia para trabajar sobre ella:

```
cp c0rrupt-mystery c0rrupt-fixed.png
```

Posteriormente se repararon los bytes dañados del encabezado y de algunos chunks internos del archivo PNG.

Después de la reparación se comprobó nuevamente el formato:

```
file c0rrupt-fixed.png
```

Una vez que el archivo fue reconocido como una imagen PNG válida, se pudo abrir y recuperar la bandera.

**Flag:**

```
academy{c0rrupt10n_1847995}
## Notas adicionales 
- La extensión o nombre del archivo no garantiza que su contenido sea de ese formato.
- Los archivos PNG comienzan con una firma conocida llamada **magic bytes**.
- Un PNG está compuesto por diferentes **chunks**, como `IHDR`, `IDAT` e `IEND`.
- Los chunks utilizan **CRC** para verificar la integridad de sus datos.
- En este reto fue necesario identificar que el archivo era un PNG corrupto y reparar su estructura para poder recuperar la bandera.
- `xxd` resulta útil para analizar archivos a nivel hexadecimal.
## Referencias
- [Archivo proporcionado por CyLab Academy](https://challenge-files.cylabacademy.net/library/8388ecc430588d15064755583476bec46e23d42a6d8de6e8995c19e40f2e4c58/c0rrupt-mystery)
- [picoCTF 2019 — c0rrupt](https://picoctf2019.haydenhousen.com/forensics/c0rrupt)