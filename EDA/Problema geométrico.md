# Un problema geométrico
#EDC/WaveletTree 
- ![[Pasted image 20211115125509.png]]
- Problema simplificado. Un punto x fila y columna.
- Fila $x$: "para la columna $i$, en que fila está el punto". ![[Pasted image 20211115125622.png]]
- Con las restricciones, la secuencia se convierte en una permutación.
- $\Sigma$ es $n$ en este caso $\to$ tamaño $nlogn + o(nlogn)$.
- Al armar WT, los que están en la parte superior se van a la izq, los que están en la parte inferior, a la der.
- ![[Pasted image 20211115130202.png]]
- ![[Pasted image 20211115130220.png]]
- ![[Pasted image 20211115130534.png]]