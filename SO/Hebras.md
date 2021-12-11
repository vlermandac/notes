# Hebras
#so/procesos #flashcards/so 
#procesos/concurrenciayparalelismo
?
## Conceptos
- Separar conceptos de proceso y hebra.
	- Proceso asociado a espacio de direccionamiento y recursos.
	- Hebra de control (thread). Instancia de ejecución mínima secuencial de CPU que require PC, SP, pila y registros.
- Comunicación entre procesos es caro.
- Hebras constituyen ejecuciones concurrentes compartiendo un espacio de direccionamiento y recursos.
	- Espacio globar compartido.
	- Pilas independientes.
- Hebras comparten más atributos que los haces más utiles que procesos multiples en ciertos casos.
![[Pasted image 20210926161727.png|500]]
- Un proceso puede tener múltiples hebras.
---
## Procesos
![[Pasted image 20210926162012.png|500]]
### [[PCB]]
---
## Implementación
### [[Hebras Kernel]]
### [[Hebras Usuario]]
---
## [[Sincronizacion de Hebras]]
<!--SR:!2021-11-10,2,230-->
