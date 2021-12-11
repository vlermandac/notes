# Laboratorio 5
Alumno: Vicente Lermanda
## 1.
- Se implementa una clase de Índice invertido con template para facilitar la instanciación con los 3 tipos de lista solicitados. ![[Pasted image 20211206150155.png]]

## 2.
- Las listas de ocurrencias se implementan con un *int_vector* y un *enc_vector*, este último con codificadores *elias gamma* y *elias delta*.
- Se quiere codificar las listas de ocurrencias para reducir el tamaño de las mismas, ya que cuando existe una muy alta cantidad de archivos, las listas pueden crecer demasiado.
- Para esto se usan los codificadores nombrados anteriormente los cuales estan basados en bits.
### Elias Gamma
- Funciona mejor para el caso donde se tienen muchos números pequeños.
- Se codifica longitud del código en unario, y luego su valor en binario.
- $2log_2(x) + 1 bit$
### Elias Delta
- Se aplica idea similar a elias gamma, pero dos veces.
- Se degrada más lento que elias Delta.
- $log_2(x) + 2log_2(log_2(x)) + 1) + 1 bit$
## 3.
- Las búsquedas tipo merge se implementaron siguiendo la idea estandar.![[Pasted image 20211206151255.png]]

## 4.
- Se quiere dividir el total de caracteres totales $C$ del dataset en 1000 partes, sin embargo sólo se logró hacer funcionar la implementación considerando $C/100$ caracteres totales, y dividiendo esto en 1000 partes.
- $C/100 = 104857600/100 = 1048576$ ![[Pasted image 20211206151753.png]]
## 5.
- Dado el tiempo considerable que tarda cada ejecución del programa, cada operación de búsqueda merge se promedia 10 veces para cada implmentación del II.
- Se ve el tiempo que tarda la operación para la implementación de II cuya lista de ocurrencia es un *int vector*, o un *enc vector* con codifador *elias gamma* y *elias delta*.

| int_vector | elias gamma | elias delta |
| ---------- | ----------- | ----------- |
| 6253.74 ms | 6870.08 ms  | 6745.22 ms  |
