# Condiciones no estandar
### Problema de min
- Multiplicar por menos uno -> obtenemos problema de max ![[Pasted image 20211127163133.png]].
- O cambiar criterio de dirección más prometedora.
	- En vez de escoger la variable que aumenta el valor, escoger la que lo disminuye más.

- Si $x_j$ no es mayor o igual a 0, cambio de variables. ![[Pasted image 20211127163420.png]] 

### Lado derecho
- Si el lado derecho de la restricción es <= 0, multiplicar por -1.
- Si la restricción son del tipo igual, usamos *variables artificiales*.
	- Las usamos para simplificar la búsqueda de base factible inicial.
	- Son positivas, pero debemos forzar a que tomen el valor 0.
	- $e(x) = b \to e(x) + a = b$
- *Método de Big-M*, penalizamos en la función objetivo las V.A.
	- $MAX \; f(x) - Ma$
	- Tomar como base inicial las variables de holgura y artificiales.
	- Realizar las operaciones por filas necesarias para eliminar la $M$ de lla función objetivo.
	- Iterar con simplex.
- *Método doble fase*
	- En la primera fase minimizamos las variables artificiales.
	- La solución encontrada define la base para la segunda fase para resolver el problema.
	
### Restricciones mayor o igual
![[Pasted image 20211127170133.png]]
- $e(x) \geq b$
- $e(x) - s + a = b$
- Resolver por Big M o doble fase.
### Resumen
![[Pasted image 20211127165817.png]]
### Casos especiales
![[Pasted image 20211127165920.png]]