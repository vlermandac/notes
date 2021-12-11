# Administración de memoria virtual
 - Ver como los procesos *ven* la memoria.
 - Los punteros, malloc, new, son direcciones de memo. virtuales.
 - ![[Pasted image 20211110125933.png]]
 ## Objetivos
 - Abstracción simple de programación.
 - Aislamiento entre procesos.
 - Asignar memoria limitada.
 - Ser eficiente.

## Mecanismos
- Se abstraer de memoria física a virtual.
- Memoria virtual habilita la ejecución de procesos sin estar completamente contenidos en memoria física.
- Procesos van pidiendo memoria cuando la necesitan, no todo de inmediato.
- Se puede llegar a usar más memoria que la disponible físicamente.
- Permite compartir memoria entre procesos (Bibliotecas compartidas).
- MMU traduce dir. virtuales a físicas.
- TLB.

## Protección de memo con particiones fijas
- ![[Pasted image 20211111155012.png]]
- Conlleva problemas de eficiencia de memoria.
## Técnicas
- [[Paginacion]]
- [[Segmentación]]