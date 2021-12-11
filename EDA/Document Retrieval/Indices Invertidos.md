# Indices Invertidos
#DocumentRetrieval
- Estructura de datos debajo de todo motor de búsqueda.
- Principal en el mundo de la recuperación de datos.
## Forma 
![[Pasted image 20211116170508.png]]
- Tabla hash es buena forma de implementarlo.
- Texto indexado se puede comprimir.
- Se puede almacenar tambien el texto al que pertenece, entre otras cosas.
## Operaciones
- *Boolean and*: Dado al menos dos palabras, devolver los archivos donde se encuentran ambas.
- Búsquedas:
	- Palabra -> recuperar la lista de ocurrencias.
	- Frase -> *intersección* de lista de ocurrencias.
## Algoritmos de intersección de listas
### Intersección de tipo merge
- Se recorren las listas en paralelo y se intersecta.
- Buena opción si $|N| \leq 20|M|$ (esto no suele ser común por la Ley de Zipf).
### Aproximación set-vs-set (SVS)
- Los elementos de la lista corta se buscan en la larga.
- Se puede buscar con búsqueda bin, seq, o exp.
- Requiere tener acceso directo dentro de la lista.
## Compresión de listas de ocurrencia
- []()Queremos comprimir teniendo en consideracción acceso directo en el caso de SVS.
- Opción trivial: Manteniendo acceso directo (compactación a k-bits).
### [[Compresion incremental]]
