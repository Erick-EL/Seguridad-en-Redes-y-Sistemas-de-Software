## Descripción 
Descomprime este archivo y busca el archivo llamado 'uber-secret.txt'.

- [Descargar archivo zip](https://artifacts.picoctf.net/c/500/files.zip)
## Solución 
```
wget https://artifacts.picoctf.net/c/500/files.zip
unzip files.zip
scripts uber-secret.txt | grep -r pico
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt:picoCTF{f1nd_15_f457_ab443fd1}

```
## Notas adicionales 
* utilice lo mismo aprendido en el reto de Big zip, al usar el grep -r para buscar en todos directorios y obtener la llave 
## Referencias
* https://webshell.cylabacademy.org/