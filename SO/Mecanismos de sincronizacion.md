# Mecanismos de sincronización
#flashcards/so 
?
- **[[Lock]]**.
- **Variables de condición**.
	- Hebra debe esperar por la ocurrencia de un evento antes de seguir. Otra avisará cuando esto ocurra.
- **Semáforos**.
	- Básicos, accesibles en SOs (llamado a sistema semget() en linux).
	- Fácil de cometer errores.
- **Monitores.**
	- Alto nivel, requiere soporte del lenguaje.
	- Más modular que semáforos, en java se usa "synchronized" como base para construirlos o Locks reentrantes.
- **Mensajes.**
	- Modelo simple de comunicación y sincronización basado en transferencia dde datos [[Atomica]] a través de un canal (send(dest, &msg), recv(src, &msg)).
	- Aplicación directa a sistemas distribuidos (RPC, Java RMI).
<!--SR:!2021-11-08,1,230-->