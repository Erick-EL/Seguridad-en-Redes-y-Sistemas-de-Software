## Descripción 
Can you break into this super secure portal?

[http://fickle-tempest.picoctf.net:53009](http://fickle-tempest.picoctf.net:53009)
What is obfuscation?
## Solución 
```
#### 1. Reconstrucción del Arreglo de Cadenas

El arreglo inicial `_0x5a46` pasa por un bucle de rotación (`shift` y `push`) que se ejecuta `0x1b4` (436) veces. Tras aplicar este desplazamiento, los valores hexadecimales pasados a la función `_0x4b5b` se traducen de la siguiente manera:

|**Clave Hexadecimal**|**Valor Traducido**|**Uso en el Código**|
|---|---|---|
|`_0x4b5b('0x0')`|`'getElementById'`|Método del DOM|
|`_0x4b5b('0x1')`|`'value'`|Propiedad del campo de entrada|
|`_0x4b5b('0x2')`|`'substring'`|Método para extraer fragmentos de texto|
|`_0x4b5b('0x3')`|`'picoCTF{'`|Fragmento 1 de la bandera|
|`_0x4b5b('0x4')`|`'not_this'`|Fragmento 2 de la bandera|
|`_0x4b5b('0x5')`|`'daf93}'`|Fragmento 4 (final) de la bandera|
|`_0x4b5b('0x6')`|`'_again_4'`|Fragmento 3 de la bandera|
|`_0x4b5b('0x7')`|`'this'`|Subcadena de control|
|`_0x4b5b('0x8')`|`'Password Verified'`|Mensaje de éxito|
|`_0x4b5b('0x9')`|`'Incorrect password'`|Mensaje de error|

#### 2. Análisis de las Condiciones (`verify`)

Con la constante `split = 4`, el código evalúa la cadena ingresada mediante múltiples verificaciones anidadas (`substring(inicio, fin)`):

1. **`substring(0, 8) == 'picoCTF{'`** → Define el inicio de la bandera (índices `0` a `7`).
    
2. **`substring(7, 9) == '{n'`** → Comprobación de solapamiento entre el prefijo y la primera palabra.
    
3. **`substring(8, 16) == 'not_this'`** → Define la segunda sección (índices `8` a `15`).
    
4. **`substring(3, 6) == 'oCT'`** → Comprobación redundante de la palabra `picoCTF{`.
    
5. **`substring(24, 32) == 'daf93}'`** → Define la sección final (índices `24` en adelante).
    
6. **`substring(6, 11) == 'F{not'`** → Comprobación de transición de caracteres.
    
7. **`substring(16, 24) == '_again_4'`** → Define la tercera sección (índices `16` a `23`).
    
8. **`substring(12, 16) == 'this'`** → Comprobación redundante dentro del segmento `not_this`.
    

#### 3. Ensamblaje de la Bandera

Ordenando los fragmentos según sus posiciones de índice en la cadena:

|**Rango de Índices**|**Fragmento**|**Cadena Acumulada**|
|---|---|---|
|**0 – 7**|`picoCTF{`|`picoCTF{`|
|**8 – 15**|`not_this`|`picoCTF{not_this`|
|**16 – 23**|`_again_4`|`picoCTF{not_this_again_4`|
|**24 – 29**|`daf93}`|`picoCTF{not_this_again_4daf93}`|
```
picoCTF{not_this_again_4daf93}
## Notas adicionales 
* Se solicita ayuda a la IA cuando sea complicado obtener un código 
## Referencias
* Gemini 
* http://fickle-tempest.picoctf.net:53009/