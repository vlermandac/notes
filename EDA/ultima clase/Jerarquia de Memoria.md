# Jerarquia de Memoria
## Motivación
- Acceder a posiciones cercanas es más cache friendly a pesar que sean asintóticamente iguales las soluciones.
## La jerarquía de memoria
![[Pasted image 20211129103330.png]]
## Modelo de memoria secundaria
- Muchos nombres distintos.
- Dos niveles, queremos minimizar transferencia entre disco a memoria ![[Pasted image 20211129104000.png]]
- Queremos establecer cotas.
	- Cota superior trivial: análisis de algoritmo en el modelo clásico. Cada dato que necesitamos tenemos que buscarlo en disco.
	- Cota inferior trivial.
	- Cell-probe: cuantos datos son accedidos. ![[Pasted image 20211129104851.png]]
## Problemas en el modelo de memoria secundaria
### Escaneo secuencial
- Acceder secuancialmente a los datos es más rápido que hacer "saltos".
- En el modelo de memoria secundaria $O(n/b)$.
### Búsqueda
- BST nos resuelven el problema de memoria óptima.
- B-trees entregan un factor de mejora para el modelo M.S.
- Es lower bound ![[Pasted image 20211129110329.png]]
- ![[Pasted image 20211129113633.png]]