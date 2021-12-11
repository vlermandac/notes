# Operaciones
#EDC/WaveletTree
- Tiempo $o(log\sigma)$.
- $access(i)$ para conocer el valor de una posición.
	- Si el bit es 0, izq. Si el bit es 1, der.
	- Para saber que elemento en el sub árbol corresponde al que estamos usando, $rank_1(B_h, i)$.
	
- $rank_\sigma(S, i)$. Cuntas veces se encuentra $\sigma$ en $S$, hasta la posición $i$.
	- Si $\sigma$ corresponde a la mitad mayor de $\Sigma$, se va a la der (o izq en caso contrario).
	- Los $n$ bits encendidos (o apagados dependiendo $\sigma$) se mapean a los valores desde 1 a $n$ del bitmap hijo.
	- Ejemplo:
		- $rank_r(S, 12)$
		- ![[Pasted image 20211115120002.png|400]]
		- 1 sola r hasta la posición 12.

- $select_\sigma(S, i)$. Donde está la $i$-ésima ocurrencia de $\sigma$.
	- Vamos desde abajo hacia arriba.
	- Partimos desde la hoja que contiene solo a $\sigma$.
	- Tomamos la $i$-ésima ocurrencia de $\sigma$.
	- Sabiendo si somos hijo der o izq (representado por 1 ó 0), revisamos la i-ésima ocurrencia de $\sigma$ en el bitmap padre, y subimos respecto al bit que corresponda.
	- Ejemplo:
		- $select_b(S, 2)$
		- ![[Pasted image 20211115121949.png]]