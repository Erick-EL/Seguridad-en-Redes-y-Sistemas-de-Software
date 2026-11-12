## Descripción 
Can you get the flag? Download this [binary](https://challenge-files.cylabacademy.net/library/394cd9dfa2b4d40f74f2ad999c1ea208ed4daf3382f56b3372ca33b69756a65d/gdbme).

Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`
## Solución 
```
academy{d3bugg3r_dr1v3_ff5329f1}
```
## Notas adicionales 
*
## Referencias