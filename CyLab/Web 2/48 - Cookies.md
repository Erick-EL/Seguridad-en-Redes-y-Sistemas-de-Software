## Descripción 
Who doesn't love cookies? Try to figure out the best one.

http://wily-courier.picoctf.net:50497/
## Solución 
```
for i in {1..20}; do curl -s http://wily-courier.picoctf.net:50497/check -H "Cookie: name=$i" | grep "picoCTF{"; done
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
```
## Notas adicionales 
* Se usa un ciclo en la terminal que contenga la curl y que obtenga la llave usando Cookie: name=$i 
## Referencias
* Terminal Kali 
* gemini 