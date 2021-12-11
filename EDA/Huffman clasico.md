# Huffman clásico
- Basado en caracteres originalmente.
- Se generan frecuencias de palabras.
- Árbol de Huffman.
- Se hace unión de los 2 caracteres menos frecuentes (greedy).
- Se etiquetan, hijo izq con 0, der con 1.
- Quedan codificados con largo máximo log n.
- Ej. ![[Pasted image 20210927115627.png]]
- Estructura del árbol debe ser almacenada junto con el texto comprimido.
- Compress ratio > 60% (pobre en el caso de lenguaje natural).