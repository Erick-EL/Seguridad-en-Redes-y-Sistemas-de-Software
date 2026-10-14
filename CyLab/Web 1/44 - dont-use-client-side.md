## Descripción 
Can you break into this super secure portal?

[http://fickle-tempest.picoctf.net:49396](http://fickle-tempest.picoctf.net:49396)
Never trust the client
## Solución 
* Inspeccionar la pagina para obtener el codigo fuente y analizar su logica en la cual esconde la llave 
```
<script type="text/javascript">
  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(0, split) == 'pico') {
      if (checkpass.substring(split*6, split*7) == 'eb02') {
        if (checkpass.substring(split, split*2) == 'CTF{') {
         if (checkpass.substring(split*4, split*5) == 'ts_p') {
          if (checkpass.substring(split*3, split*4) == 'lien') {
            if (checkpass.substring(split*5, split*6) == 'lz_2') {
              if (checkpass.substring(split*2, split*3) == 'no_c') {
                if (checkpass.substring(split*7, split*8) == 'b45}') {
                  alert("Password Verified")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");

```
## Notas adicionales 
* En casos de no entender la logica, podemos recurrir a la IA a que nos aliviane 
## Referencias
* Gemini
* http://fickle-tempest.picoctf.net:49396/