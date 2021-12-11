# Tipos de compresores
## Clasificación por proceso de modelado
- Se refiere a cómo detectan los símbolos y obtienen info sobre los mismos.
### Compresión estática
- Un símbolo recibe siempre el mismo código.
- Ej. Clave morse.
### Compresión en 2 pasadas o semi-estática
- Se recorre el texto una primera vez para obtener decidir que códigos asignar.
- Finalmente se comprime el texto.
- Ej. Huffman clásico.
### Compresión dinámica
- Se procesa símbolo a símbolo.
- Mientras se avanza, se ajusta el esquema de codificación.
- Códigos asignados a un mismo símbolo pueden variar.
- Ej. Compresores de diccionario, Lempel-Ziv, Huffman dinámico, etc.
