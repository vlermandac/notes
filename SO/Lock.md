# Locks
#flashcards/so 
?
- Semántica mínima, sirven para construir otros mecanismos más complejos.
- Objeto de memoria que proporciona las siguientes operaciones:
	- acquire()/ lock(): Hebra la llama antes de entrar a SC. Atómica.
		- No retorna hasta que hebra consigue lock.
	- release()/ unlock(): Hebra la llama después de salir de SC.
- Exclusión mutua dado por par de llamadas acquire, release.
	- Entre llamada de estas, hebra se mantiene en stock.
- 2 tipos de lock:
	- Spinlocks (no bloqueante. espera ocupada (busy-waiting)).
	- Mutex (bloqueante).
- Lock bloqueante, llamar primitiva, cuando no esta disponible el lock, se bloquea.
## Spinlocks
- Arquitectura de cpu proporciona instrucción atómica.
- *Test and set* (atómica).
- No hay garantía de obtención de lock de las hebras.
- Requieren usar CPU, esto puede producir overhead si muchas hebras quieren entrar.
- Pregunta todo el tiempo si puede usar el lock, usa ciclos de CPU.
### Spinlock basado en colas
- Fetch-and-add.
- Spinlocks con tickets.
- Compare-and-swap, maneja concurrencia.
<!--SR:!2021-11-08,1,230-->