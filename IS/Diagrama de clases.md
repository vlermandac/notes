# Diagrama de clases: Esquema Conceptual

## Identificar atributos
- Atributos de dominio simple.
- Ante la duda de atributo o concepto, modelar como concepto.
- A partir de los conceptos relevantes del diagrama de secuencia y el escenario principal de éxito.

## Identificar asociaciones
- Relaciones enre conceptos.
- Evitar redundancia.

## Ejemplo caja supermercado
- Conceptos extraídos de un solo caso de uso (de éxito).
![[Pasted image 20211207125200.png]]
- Orden de lectura (no normal en otros dominios), una venta se realiza en 1 y solo 1 caja. Mientras una caja realiza 0 a muchas ventas. 
- Cada clase solo encapsula atributos de ellos mismos.
- Si se necesita un dato de otra clase, se "pide" a traves de las asociaciones.
	- Ej. Venta solicita idCaja a Caja.

### Clase asociación
![[Pasted image 20211207131157.png]]	
## Mecanismos de abstracción
- **Clases.**
- Clasificación / Instanciación.
- Composición / Descomposición
- Agrupación / Individualización.
- Especialización / Generalización.
![[Pasted image 20211207135013.png]]
- Ejemplo ![[Pasted image 20211207135051.png]]

## Agregación
- Por valor o composición.
	- Tiempo de vida del objeto dependiente del que lo incluye.
	- Rombo negro.
- Por referencia o agregación.
	- Tiempo de vida independiente.
	- Rombo blanco.

![[Pasted image 20211207161120.png]]
![[Pasted image 20211207161554.png]]
- Clasificaciones estáticas vs dinámicas ![[Pasted image 20211207161658.png]]
- Herencia múltiple (no se recomienda). ![[Pasted image 20211207161748.png]]
![[2021_09 [INGSW1] Implementación de Clases 1.pdf]]

- Ejemplo cardinalidad 1 a muchos. ![[Pasted image 20211208222012.png]]