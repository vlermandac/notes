# Simplex tabular
#simplex
## Descripción 
1. Encontrar base factible.
2. Mientras exista dirección de mejora:
	1. Encontrar *variable no básica* de entrada: dir. más conveniente de Z (f. objetivo).
	2. Encontrar una *variable básica* de sálida: la primera que se hace 0 al aumentar el valor de la variable no básica de entrada.
	3. Ajustar los valores de las variables a la nueva base: método Gauss-Jordan.
## Ejemplo
- Primer caso consideramos x e y como variables no básicas (iguales a 0).
![[Pasted image 20210930212615.png]]
![[Pasted image 20211002231428.png]]
- $$y$$ corresponde a dir. más prometedora.
![[Pasted image 20211002232913.png]]
![[Pasted image 20211003115040.png]]
![[Pasted image 20211003115119.png]]
![[Pasted image 20211003115143.png]]
![[Pasted image 20211003115200.png]]