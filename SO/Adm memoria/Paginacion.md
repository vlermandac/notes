# Paginación
#adm_memo/tecnicas
- Mecanismo para implementar memo virtual.
- Técnica actual.
- Pra solucionar el problema de [[fragmentacion externa]] dada con particiones variables. Usar particiones fijas en memoria virtual y física.
- ![[Pasted image 20211114130545.png]]
- Se mapea virtual a física (invisible al programa).
- ![[Pasted image 20211114131517.png]]
- ![[Pasted image 20211114132533.png]]
- ![[Pasted image 20211114133800.png]]
- ![[Pasted image 20211114134303.png]]
- ![[Pasted image 20211115152939.png]]
- ![[Pasted image 20211115153423.png]]
## Resumen
- Usa mucha memoria en tablas de página.
- Memoria física dividida en marcos de página de igual tamaño.
- Mismo tamaño que las páginas virtuales (no existen perse).
- Usa tabla de página para mapear págunas virtuales a físicas.
- Página: página virtual.
- Marco: página física.