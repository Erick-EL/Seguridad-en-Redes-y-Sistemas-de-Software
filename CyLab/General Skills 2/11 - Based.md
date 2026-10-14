## Descripción 
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?
## Solución 
``` 
nc fickle-tempest.picoctf.net 50805
Let us see how data is stored
pie
Please give the 01110000 01101001 01100101 as a word.
...
you have 45 seconds.....

Input:
pie
Please give me the  o154 o151 o172 o141 o162 o144 as a word.
Input:
lizard
Please give me the 6f76656e as a word.
Input:
oven
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_bf1F59A2}
```
## Notas adicionales 
* se abrieron 3 ventanas extra de cyberchef para las conversiones y agilizar el tiempo 
* se hicieron las conversiones de binario, octal y hexadecimal
## Referencias
* https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)&input=MDExMTAwMDAgMDExMDEwMDEgMDExMDAxMDE&oeol=FF
* https://webshell.cylabacademy.org/