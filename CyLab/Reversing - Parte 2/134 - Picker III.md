## Descripción 
Can you figure out how this program works to get the flag? Connect to the program with netcat:

`$ nc chatelaine.cylabacademy.net 22259`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/0c20c076e50e377ab1ba1e162d33f882ab2caaa6c6766d463bf0af50cdd59d4a/picker-III.py).
## Solución 
```
┌──(kali㉿kali)-[~]
└─$ nc chatelaine.cylabacademy.net 22259
==> help

This program fixes vulnerabilities in its predecessor by limiting what
functions can be called to a table of predefined functions. This still puts
the user in charge, but prevents them from calling undesirable subroutines.

* Enter 'quit' to quit the program.
* Enter 'help' for this text.
* Enter 'reset' to reset the table.
* Enter '1' to execute the first function in the table.
* Enter '2' to execute the second function in the table.
* Enter '3' to execute the third function in the table.
* Enter '4' to execute the fourth function in the table.

Here's the current table:
  
1: print_table
2: read_variable
3: write_variable
4: getRandomNumber
==> 3
Please enter variable name to write: getRandomNumber
Please enter new value of variable: win
==> 4
0x61 0x63 0x61 0x64 0x65 0x6d 0x79 0x7b 0x37 0x68 0x31 0x35 0x5f 0x31 0x35 0x5f 0x77 0x68 0x34 0x37 0x5f 0x77 0x33 0x5f 0x67 0x33 0x37 0x5f 0x77 0x31 0x37 0x68 0x5f 0x75 0x35 0x33 0x72 0x35 0x5f 0x31 0x6e 0x5f 0x63 0x68 0x34 0x72 0x67 0x33 0x5f 0x39 0x34 0x38 0x65 0x38 0x36 0x36 0x65 0x7d 
==>                              
academy{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_948e866e}
```
## Notas adicionales 
* Al ingresar al servidor y dar el comando help te da distintas opciones en las cuales una vienen con la opción de modificar la variable, así que aprovechamos eso y modificamos de forma que nos arroje la bandera en una cadenas que después pasamos a ciberchef para decodificar la bandera real 
## Referencias
* https://gchq.github.io/CyberChef/