## Descripción 
Can you make sense of this file?

Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).
* Multiple decoding is always good.
## Solución 
```
:~$ wget https://artifacts.picoctf.net/c/471/enc_flag

:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt  enc_flag  file  flag  ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt  strings  warm
:~$ cat enc_flag
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFpSV0VKWVZGVmtNRTVHV2tWU2JYUlVDbUpXV25sVWJGcHZWbGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==              

```

* picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
## Notas adicionales 
* Descargamos el archivo y obtenemos su contenido el cual hay que decodificar múltiples veces hasta obtener la bandera 
## Referencias
* https://www.base64decode.org/es/