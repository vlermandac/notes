# Van Emde Boas Tree
- Objetivo, realizar operaciones succ/pred en tiempo $o(log\;n)$ (o chica).
- Para word-RAM: $O(log\;w) = O(log\;log\;u)$ con espacio $\theta(u)$.
- Mejoramos las cotas previas.
- Dividimos en raíz de u, bloques.
- $T(u) \leq T(\sqrt{u}) + O(1)$
### Coordenadas jerárquicas
- Dado un entero $x$, lo representamos por $x = <c,i>$.
	- $c = x / \sqrt{u} \to$ determina el bloque.
	- $i = x \% \sqrt{u} \to$ índice dentro del bloque.
	- Notar que $x = c \cdot \sqrt{u} + i$.
### Forma
- Se define recursivamente, cada una de las "cajas", son un VEBtree con un universo más pequeño.
- Solo el max se almacena recursivamente.
![[Pasted image 20211122160807.png]]
- Se hace recursión solo en los bloques, o sólo en el resumen.
## Operaciones
### Sucesor
- $SUC(V, x = <c, i>)$
	- $if \; x < V.min, \; \; return \; V.min$
	- $if \; i < V.bloque[c].max, \; \; return \; <c, SUC(V.bloque[c],i)>$
	- $else \; c' = SUC(V.resumen, c), \;\;  return \; <c', v.bloque[c'].min>$
![[Pasted image 20211122173759.png]]
### Insertar
- $INS(V, x = <c,i>)$
	- $if \;\; V.min = none, \; \; V.min = V.max = x, \; \; return$. (caso estruct. vacía).
	- $if \;\; x < V.min, \;\; swap(x, V.min)$ continua...
	- $if \;\; x > V.max, \;\; V.max = x$ continua...
		- $if \;\; V.bloque[c].min = none$
			- $INS(V.resumen, c)$
		- $INS(V.blque[c], i)$
### Borrar
## Reducción en espacio
## Representación alternativa
## Van Emde Boas layout
## Indirección
