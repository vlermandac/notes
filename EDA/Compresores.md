# Compresores estáticos y dinámicos
#compresion 
- Estaticos. Ej. clave morse.
- Semi estático.
	- Recorre el texto anteriormente.
- Dinámico.
	- Toma medidas a medida que ve los símbolos.
- Compresores estadísticos com Huffman son compresores de *orden 0* (asumen que símbolos son independientes entre si).
### Teoría de la información 
#### Shannon
![[Pasted image 20210927112259.png]]
#### Entropía
![[Pasted image 20210927112930.png]]
- Queremos minimizar redundancia.
- Entropía es lower bound de cantidad de bits de compresiones*orden 0* (objetivo).
- P2 es más compresible (entropía menor) ![[Pasted image 20211016200313.png]]