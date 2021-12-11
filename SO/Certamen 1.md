# Certamen 1 
Alumno: Vicente Lermanda C.
Profesora: Cecilia Hernandez.

## 1.
### a)
![[Pasted image 20211108175229.png]]
### b)
- $a$ es el valor de pid del proceso padre original. Se imprime 8 veces, 1 vez por proceso.

## 2.
### a)
- $H1$ puede modificar a $x$ si $flag2$ es false. Esto ocurre cuando $H2$ aún no se ha ejecutado, o si $H1$ alcanza a salir del while antes que $H2$ comience y convierta $flag2$ en true.
### b)
- De manera análoga, $H2$ puede modificar a $x$ si $flag1$ es false. Esto ocurre cuando $H1$ aún no se ha ejecutado, o si $H2$ alcanza a salir del while antes que $H1$ comience y convierta $flag1$ en true.

### c)
- Si, ya que una vez que se ejecute $H1$ o $H2$, el otro va a quedar atrapado en el while hasta que el primer proceso termine. Esto es parecido a un spinlock, pero de más alto nivel, ya que se utilizan flags booleanas.

### d)
- Si trae otros problemas, ya que si se llegan a ejecutar al mismo tiempo, al volverse las dos flag true, ambas quedarán atrapadas en el while, generandose así un $deadlock$.
### e)
Se puede mejorar para que se asemeje al algoritmo de Drekken.
```C
bool flag1 = false, flag2 = false;
int turno = 0, x = 0;

//H1:
flag1 = true;
while(flag2){
	if(turno == 1){
		flag1 = false;
		while(turno == 1);
		flag1 = true;
	}
}
x++;
turno = 1;
flag1 = false;

//H2:
flag2 = true;
while(flag1){
	if(turno == 0){
		flag2 = false;
		while(turno == 0);
		flag2 = true;
	}
}
x--;
turno = 0;
flag2 = false;
```
## 3.
## 4.
### a)
- Verdadero.

### b)
- Falso, se privilegian procesos interactivos por sobre intensivos en la CPU.

### c)
- Falso, para compartir datos entre procesos se pueden crear espacios de memoria compartida o usar pipes, entre otros mecanismos. Sin embargo, los que si comparten el Heap son las hebras.

### d)
- Falso, el deadlock produce inanición de los procesos involucrados en él.

### e)
- Verdadero.