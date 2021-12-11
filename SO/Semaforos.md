# Semáforos
#so/procesos #flashcards/so/procesos/hebras 
#flashcards/so 
?
- Primitvas en el kernel.
- Más alto nivel que locks.
- No solo mutex, sino que define planificaciones también.
- Objeto atómico con valor y cola de espera.
- 2 operaciones.
	1.  wait(sem)/down(dem)/ P(sem).
		- Se le puede definir un valor inicial.
		- Decrementa el valor del semáforo. Sem.valor--.
		- if(sem.valor < 0) bloquea hebra (agrega a la cola de espera).
		- Else hebra puede entrar a SC.
	2. V(sem)/Signal(sem)/Up(sem).
		- Sem.valor++.
		- if(Existe hebra en cola de espera) despierta una.
![[Pasted image 20210927125628.png]]
- Con el valor inicial del semaforo uno especifíca la cantidad de hebras que pueden acceder al código a la vez.
### Problemas con semáforos
- Al ser variables globales pueden ser accesadas por cualquier hebra directamente (no buena para IS).
- No hay conexión entre semáforo y recurso al que se quiere accesar.
- Fácil de cometer errores.
<!--SR:!2021-11-08,1,230-->