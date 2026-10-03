## Descripción 
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.

[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/ce53ef9432bf367be41e465224d721c1187c39debcd758efcd28e99a6b7ff7a4/Addadshashanammu.zip)
## Solución 1
```
wget https://challenge-files.picoctf.net/c_wily_courier/ce53ef9432bf367be41e465224d721c1187c39debcd758efcd28e99a6b7ff7a4/Addadshashanammu.zip

strings Addadshashanammu.zip | grep pico
printf("*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}\n");

```
## Solución 2
```
unzip Addadshashanammu.zip                                  
:~$ ls  
Addadshashanammu  Addadshashanammu.zip  README.txt  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ cat fang-of-haynekhtnamet.c
#include <stdio.h>


int main(){
printf("*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}\n");
}
```

## Notas adicionales 
* ctrl a - va al inicio de la linea del comando 
* ctrl e - va al final de la linea del comando 
* unzip - para descomprimir archivos .zip
* cd - posicionarme en un directorio 
## Referencias
* https://webshell.cylabacademy.org/