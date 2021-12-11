# Certamen año pasado
## Pregunta 1
### a)
- IniciarEncuesta(dia).
	- Se crea intancia RespuestaDiaria.
	- Se actualiza el valor del atributo dia.
	- Se actualiza el valor del atributo terminada a false.
	- Se asocia la instancia RespuestaDiaria a objeto Dosis, se comparan fechas entre ambas.

- ResponderReacconZonal(tipo, gravedad, comentario).
	- Se crea instancia ReaccionZonal.
	- Se actualiza valor del atributo tipo con argumento tipo.
	- Se actualiza valor del atributo gravedad con argumento gravedad.
	- Si se hace un comentario (comentario no nulo):
		- Se crea instancia ComentarioRZ.
		- Se actualiza el atriuto comentarioZ con valor del argumento Comentario.
		- Se asocia comentarioRZ con instancia de ReaccionZonal.

- ResponderReaccionGeneral(tipo, gravedad, comentario):
	- IDEM.

- terminarEncuesta()
	- Se actualiza valor de atributo terminada a verdadero.
	
	
### b)
