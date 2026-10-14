## Descripción 
🥛 [http://chatelaine.cylabacademy.net:40890/](http://chatelaine.cylabacademy.net:40890/)
## Solución 
```
┌──(kali㉿kali)-[~/cylab]
└─$ RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg -a concat_v.png | grep academy
b1,b,lsb,xy         .. text: "academy{imag3_m4n1pul4t10n_sl4p5}
```
## Notas adicionales 
* El error `SystemStackError: stack level too deep` ocurre porque **la imagen `concat_v.png` tiene una altura vertical (o número de scanlines) demasiado grande**, lo que provoca que la biblioteca `zpng` (usada por `zsteg`) agote la pila de llamadas de Ruby debido a un algoritmo recursivo mal optimizado para procesar los filtros de las filas de la imagen
*  Puedes forzar a Ruby a asignar más espacio para la pila de ejecución antes de lanzar `zsteg`. Ejecuta el comando configurando la variable de entorno `RUBY_THREAD_VM_STACK_SIZE`
## Referencias
* Gemini 