## Descripción 
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.
## Solución 
```Son69-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/9e4f9113960f157ceb824bdb449dc2a74504b484346c1442e64854408d5a90c5/file
Son69-academy@webshell:~$ ls 
README.txt  file
Son69-academy@webshell:~$ cat file | grep pico
```
picoCTF{grep_is_good_to_find_things_9C6Ef2F7}
## Notas adicionales 
*  Primero descargue el archivo https://challenge-files.picoctf.net/c_fickle_tempest/9e4f9113960f157ceb824bdb449dc2a74504b484346c1442e64854408d5a90c5/file
* verifico que se descargo 
* y por ultimo hago un grep para encontrar la cadena especifica en el archivo 
## Referencias
* https://webshell.cylabacademy.org/