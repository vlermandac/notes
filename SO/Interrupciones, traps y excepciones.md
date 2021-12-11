# Interrupciones, traps y excepciones
#flashcards/so 
?
- SO tiene rutinas de atención para manejar estas.
- Vector de interrupciones almacena dirección a rutinas de atención.
- Manejador de estados no se bloquea y debe ejecutarse independiente del estado del proceso.
- Transferencia de código de usuario a atención de rutina debe ser [[Atomica]].
- Transparente a usuario.
## [[Interrupciones]]
## Excepciones
- Sincrónicas.
- Causadas por eventos inesperados en la ejecución de código.
- Programa terminado.
- No ocurren en escritura a memoria.
## Traps
- Sincrónicos.
- Programador las introduce en código para pedir servicio a SO.
- También llamadas interrupciones SW.
<!--SR:!2021-11-08,1,230-->