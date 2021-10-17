# Huffman
#compresion 
- Compresión estadística semiestática.
### 2 pasos:
- Calcular frecuencias de los símbolos de entrada y codificar.
- Compresión. 
![[Pasted image 20211016202325.png]]
## Huffman clásico
- Basado en caracteres originalmente.
- Se generan frecuencias de palabras.
- Árbol de Huffman.
- Se hace unión de los 2 caracteres menos frecuentes (greedy).
- Se etiquetan, hijo izq con 0, der con 1.
- Quedan codificados con largo máximo log n.
![[Pasted image 20210927115627.png]]
