## Descripción 
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.cylabacademy.net/library/53f38374e47a48424dc7e9100aba4e4b42a590f3921cfc31188171ae7d6d61e3/whitepages.txt) is all blank!
## Solución 
```
	... with open('whitepages.txt', 'rb') as f:
...     data = f.read()
... 
... # Intercambiamos la asignación de bits:
... # Espacio normal (\x20) -> '1'
... # Em Space (\xe2\x80\x83) -> '0'
... binary_str = data.replace(b'\xe2\x80\x83', b'0').replace(b'\x20', b'1').decode('\
ascii')
... 
... flag = ""
... for i in range(0, len(binary_str), 8):
...     byte = binary_str[i:i+8]
...     if len(byte) == 8:
...         flag += chr(int(byte, 2))
... 
... print(flag)
... 

academy

SEE PUBLIC RECORDS & BACKGROUND REPORT
5000 Forbes Ave, Pittsburgh, PA 15213
academy{not_all_spaces_are_created_equal_19fc1787ee14ef2c56ee0cddc142a0d9}
```
## Notas adicionales 
- **Inspección Hexadecimal:** Al encontrarse con un archivo aparentemente "vacío", el primer paso analítico es inspeccionar sus bytes con utilidades como `xxd` o `hexdump` (`xxd whitepages.txt | head`). Esto revela inmediatamente la presencia de patrones repetitivos en formato hexadecimal.
    
- **Diversidad de Espacios en Unicode:** El estándar Unicode define múltiples caracteres de espacio sin representación visual directa (_Zero-Width Space_, _En Space_, _Em Space_, _Non-Breaking Space_).
    
- **Uso en Ciberseguridad:** Además de retos de esteganografía, el uso de caracteres invisibles o de ancho cero se emplea en técnicas reales de evasión (_homoglyph attacks_, marcas de agua en texto para trazabilidad de filtraciones y evasión de filtros anti-spam/phishing).
## Referencias
- **Página oficial de picoCTF:** [picoctf.org](https://picoctf.org/)
    
- **Tabla de caracteres Unicode (General Punctuation / Space Characters):** [unicode.org/charts](https://www.unicode.org/charts/)
    
- **CyberChef (Herramienta multiuso para decodificación):** [gchq.github.io/CyberChef](https://gchq.github.io/CyberChef/)