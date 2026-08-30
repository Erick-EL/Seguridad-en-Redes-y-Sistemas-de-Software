## Descripción 
How to automate tasks to run at intervals on linux servers?

Use ssh to connect to this server:

`Server: saturn.picoctf.net Port: 61070 Username: picoplayer Password: ENAFb6zfzn`
## Solución 
```
ssh -p 61070 picoplayer@saturn.picoctf.net

picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}
```
## Notas adicionales 
* las tareas programadas (conocidas como _cron jobs_) se configuran en archivos específicos
* el archivo de configuración global del sistema donde se definen estas tareas se llama crontab y este archivo maestro se encuentra casi siempre en el directorio /etc
## Referencias
* https://webshell.cylabacademy.org/
* El buen google 