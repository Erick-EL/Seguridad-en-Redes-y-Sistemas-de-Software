## Descripción 
Can you win in a convincing manner against this chess bot? He won't go easy on you! You can find the challenge [here](http://xebec.cylabacademy.net:35415/).
## Solución 
se abrió la consola de desarrollador del navegador mediante:
F12 → Console
Se analizó cómo el cliente se comunica con el servidor mediante WebSocket. El código utiliza una conexión WebSocket y envía mensajes relacionados con la evaluación de la posición del tablero.
Normalmente, el cliente envía una evaluación generada por Stockfish. Sin embargo, el servidor confía directamente en el valor recibido y no comprueba que corresponda realmente a la posición del tablero.
Se aprovechó esta situación enviando manualmente una evaluación negativa muy grande:
ws.send("eval -100000")
El valor negativo hace que el servidor interprete que Stockfish está perdiendo por una cantidad muy grande. Como consecuencia, el bot considera la posición perdida y se rinde
academy{c1i3nt_s1d3_w3b_s0ck3t5_906748f0}
## Notas adicionales 
* La evaluación puede manipularse enviando manualmente un mensaje al WebSocket.
* El ataque consiste en modificar un dato enviado por el cliente para alterar la decisión del servidor.
- Este tipo de problema se relaciona con la falta de validación de datos controlados por el cliente
## Referencias