# Llamadas a sistema
### Algunas llamadas
- [[fork]]()
- [[exec]]()
- [[wait]]()
### Conceptos
- Caso linux (no procesos, sino tasks).
- Operación [[Atomica]] (permite cambiar de modos sin problemas).
	- Salva PC, SP.
	- Setea modo kernel.
	- Setea el PC a rutina de atención de llamada.
- Parten en modo usuario, finalmente deben pasar a modo kernel.
![[Pasted image 20210924170834.png]]
### Distinto a API
- API: definición de función o procedimiento que especifíca como obtener determinado servicio.
- LLamada a sistema: requerimiento específicio hecho al kernel usando una trap.
- Normalmente cada llamada a sistema tiene una rutina wrapper que defina la API que programadores deben usar.
- Una API de una biblioteca puede incluir más de una llamada a sistema.
- Desde un punto de vista del programador no importa la distinción entre ambos.
- glib es un wrapper.
### Ejemplo
![[Pasted image 20210924172301.png]] 
![[Pasted image 20210925154701.png]]