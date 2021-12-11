# Laboratorio 4
Alumno:   Vicente Lermanda C.
Profesor:  Diego Seco N.
Ayudante: Alexander Irribara C.

## 1.
### Sparse Table
- En una tabla se almacenan los mínimos de todos los rangos de tamaño potencia de 2 obtenibles en el arreglo. Para obtener el RMQ se comparan dos sub-arreglos de la tabla. Para un rango de búsqueda $[i, j]$ se obtiene su logaritmo en base 2 piso $k$, y se compara el mínimo entre los sub-arreglos de tamaño $2^k$, que empiezan en $i$ y en $j - 2^k + 1$. 
### Segment Tree
- Corresponde a un árbol binario construido en base a un arreglo, donde cada nivel del arreglo representa un rango potencia de 2 (hojas $2^1$, altura 1 $2^2$ y así) y cada nodo representa la query para el rango que cubre.
	Para obtener el RMQ se busca desde la raíz hacia abajo. Si el rango del nodo que se está visitando actualmente está contenido en el rango de la query, se obtiene y se compara con los demas nodos que cumplen esta condición.
## 2
### Resultados
- Se considera un tamaño creciente entre 1 y 100000 aumentando en potencias de 10.
- Ejes log x log para mejor visualización.
- Para cada ejecución se obtiene el tiempo medio de 100 repeticiones.
#### Construcción
![[Pasted image 20211101161820.png]]
#### RMQ
- Se consideran rangos aleatorios.
- ![[Pasted image 20211101162141.png]]