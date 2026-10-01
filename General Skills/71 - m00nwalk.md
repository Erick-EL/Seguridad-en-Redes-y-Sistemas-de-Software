## Descripción 
Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.
## Solución 
```
pip install git+https://github.com/colaclanth/sstv.git
hash -r
sstv -d message.wav -o flag.png
```
## Notas adicionales 
- **Fundamento de SSTV:** La Televisión de Barrido Lento modula la luminancia y los componentes de color (RGB) de cada línea de la imagen en frecuencias de audio dentro del espectro audible (aproximadamente entre 1200 Hz y 2300 Hz).
    
- **Modos de transmisión:** Existen distintos estándares de SSTV (`Scottie 1`, `Martin 1`, `Robot 36`, etc.), los cuales varían en la resolución, el tiempo de escaneo por línea y las señales de sincronización. La herramienta `sstv` analiza el código de cabecera VIS (_Vertical Interval Signaling_) para seleccionar el modo de forma automática.
    
- **Herramientas alternativas:** En entornos con interfaz gráfica (GUI), se emplean herramientas como **QSSTV** (Linux) o **MMSSTV** (Windows) para procesar el audio mediante la tarjeta de sonido en tiempo real.
## Referencias
- **Página oficial de picoCTF:** [picoctf.org](https://picoctf.org/)
    
- **Repositorio oficial del decodificador SSTV (colaclanth):** [github.com/colaclanth/sstv](https://github.com/colaclanth/sstv)
    
- **Documentación sobre el estándar SSTV:** [ARRL - Slow Scan Television](https://www.google.com/search?q=http://www.arrl.org/sstv)