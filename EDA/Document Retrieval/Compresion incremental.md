# Compresión Incremental de listas
- Buena capacidad de compresión.
- Aprovechamos que las listas de ocurrenicas son crecientes.
- Guardamos los valores respecto a sus diferencias con el número anterior.
- Aún debemos lidiar con el acceso directo, para conocer un elemento en $i$, hay que descomprimir desde 0 hasta $i-1$.
- Para mantener acceso directo hacemos la diferencia con el 1er elemento (comprime mucho menos).
![[Pasted image 20211116184658.png]]
- Para representar los números pequeños generados por las diferencias, los codificamos con Elias Gamma, o Elias Delta.