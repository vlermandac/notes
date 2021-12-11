# Sincronización
#so/procesos #hebras 
#flashcards/so 
?
-  Pueden ocurrir en cualquier momento.
-  Ejecución entrante puede ocasionar problemas en la ejecución del proceso que fue interrumpido.
-  SO debe evitar estos problemas sincronizando los procesos.
- Garantiza que secuencia corta de instrucciones se ejecute [[Atomica]]mente (como si fuera una).
	- Se logra deshabilitando interrupciones antes de secuencia y habilitando después.
	- Arquitectura provee de instrucciones atómicas.
	- *Test and set*: Escribir en posición de memoria y retornar valor antiguo atómicamente, *compare and swap*.
	---
	## [[Sincronizacion de Hebras]]
<!--SR:!2021-11-10,3,250-->


