# Teoría de la información de Shannon
- La cantidad de información equivale a la cantidad de *novedad* en el mensaje.
- Queremos encontrar el número mínimo de bits para codificar una respuesta.
- Dado un número de $k$ digitos en base $n$.![[Pasted image 20211118162408.png]]
- Para textos,
	- Alfabeto de $n$ símbolos.
	- Si enviamos por un canal $s$ símbolos por segundo:
	- $H = s\;log_2n$
	- $H$: cantidad de info (en bits), enviada por segundo.

- Si el símbolo $a_i$ ocurre con probabilidad $P_i$, entonces ocurre $sP_i$ veces por unidad de tiempo.
	- Considerar que $P_1 + P_2 + \dots + P_n = 1$.
- (Caso) Si todos los $P_i$ son iguales:
	- $P_i = P$
	- $1 = \sum P_i = nP$
	- $n = 1/P$
	- $\implies H = s\;log_2 n \implies H = s\;log_2(1/P) = -s\; log_2 P$
	- $H/s = H_0 = -log_2(P)$
	
- Como H es la cantidad de información enviada (en todos los símbolos) por segundo. La información contenida por *un* símbolo en base $n$ es $H/s = -\sum P_i \; log_2(P_i) = \sum P_i \; log_2(1/P_i)$.
- Esta entropía nos indica la mínima cantidad de bits para codificar cada uno de los símbolos.
- Limite inferior de la compresión (para orden 0 ($H_0$)).