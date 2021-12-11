# Modos e instrucciones protegidas de operación
#so/hw #flashcards/so 
?
## Modo kernel y modo usuario
- Instrucciones de HW permitan cambiar de un modo a otro.
- Espacios de MV puedes ser marcados como parte de espacio de usuario o kernel.
- Intentar acceder en modo usuario a memoria en el espacio del kernel resulta en excepción.
- El modo kernel puede acceder a ampos espacios de memoria.
## Instrucciones privilegiadas
- Arquitectura soporta modo de operación protegido.
- Solo se ejecutan en modo kernel.
- Los programas de usuario puede accesar a los recursos pasando de modo usuario a modo kernel.
	- [[Interrupcion]]es (del timer y E/S).
	- [[Excepcion]]es.
	- Traps.
- *Cambio de contexto*: SO cambia de ejecución de un proceso a otro.
## Protección de memoria
- HW registros especializados relcionados al manejo de la memoria virtual.
## Cambio de modo
- Transferencia atómica.
	- [[Atomica]] (no sé interrumpa).
	- Operación atómica cambia:
		- PC, SP, protección de memoria, modo kernel/usuario.
- Usuario no se da cuanta que hay un cambio.
<!--SR:!2021-11-09,1,210-->
