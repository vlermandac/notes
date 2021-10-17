# Alfabeto de entrada
- Existen técnicas basadas en carácteres y en palabras.
- Puede ser fijo o variable.
	- Ej. leer de a 2 caracteres, vs leer 1, despues 3, despues 2, etc.
## Caracteres
- Vocabulario pequeño.
- Texto tiene millones de símbolos.
## Palabras
- Vocabulario: miles de palabras distintas.
- Número de símbolos a procesar es menor.
## Puede ser mejor usar palabras en vez caracts.?
- Si. Las palabras son la base del procesado de texto en recuperación de texto e indexación.
- [[Ley de Heaps]].
- [[Ley de Zipf]].
## Output
- Asignamos codigos más cortos a símbolos de entrada más frecuentes.
- Decidir si trabajar a nivel de bits o bytes.
- Técnicas orientadas a byte vs orientadas a bit.
- Bit mejora la compresión, más dificil de descomprimir.
- Bytes comprime menos; más fácil de descomprimir.
- Actualmente esto ya no aplica tanto.
![[Pasted image 20210927105949.png]]