# Sincronización de hebras
#flashcards/so/procesos/hebras 
	- Hebras ejecutan sus instrucciones en forma entrelazada.
	- No se pueden asumir tiempos de ejecución (nunca usar sleep() para demorar ejecución).
### Compartición de recursos
- El acceso de recursos entre las hebras debe permitirse de forma controlada.
- Mecanismos para controlar accesos tales como Locks, mutexes, variables de condición, semáforos y monitores.
- Recursos compartidos en hebras.
	- Variables globales y memoria dinámica.
- Recursos compartidos en procesos.
	- Archivos, puertos de conexión.
### Cómo resolver problemas?
- **[[Mecanismos de sincronizacion]]**
- Sólo una hebra a la vez puede acceder a recurso compartido.
- *Exclusión mutua*.
- Segmento de código que accesa a recurso compartido se llama "sección crítica".
- Idea es que sólo se proteja sección crítica y no otro código.
### Definiciones
- **Condición de carrera**: salida de programa concurrente depende del orden en que se ejecutan las instrucciones produciendo inconsistencias.
- **Exclusión mutua**: sólo una hebra a la vez puede accesar recurso compartido.
- **Sección crítica**: segmento de código que sólo una hebra a la vez puede ejecutar.
	- *Requerimientos*:
		- *Progreso*: si una hebra no está en SC no debe impedir que otra entre.
		- *Espera finita*: si una hebra esta esperando entrar a SC, eventualmente debe tener éxito.
		- *Eficiencia*: la sobrecarga de uso de sincronización debe ser mucho menor que el tiempo de ejecución de SC.
- **[[Deadlock]]**.
#### Primitivas de sincronización
- **[[Lock]]**: primitiva básica para asegurar exclusión mutua, asegurando que sólo una hebra a la vez pueda accesar a sección crítica.
- **[[Semaforos]]**.
- **[[Variables de condicion]]**
- **[[Barreras]]**
- **[[Monitores]]**.
## Problemas clásicos
### [[Problema productor_consumidor]]
### [[Problema lectores_escritor]]
### [[Problema de filosofos comensales]]
