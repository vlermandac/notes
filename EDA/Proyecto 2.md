# Proyecto II: Estructuras de Datos Compactas
## Introducción
## Ejercicios
### 1.
- Para calcular la entropía de orden 0, se utiliza la fórmula de la entropía de Shannon.
- Se utiliza una tabla hash donde se almacena la frecuencia de cada elemento $x$ distinto del dataset.
- $p(x) = freq \; de \; x / total \; de \; datos$
- $H_0 = - \Sigma \; p(x) \cdot \log_2p(x)$
![[Pasted image 20211128214253.png]]
### 2.
- Se lee el dataset archivo por archivo, y cada matriz se almacena en row major order, en un único vector.
- Posteriormente, los valores de ese vector se traspasan a un sdsl::int_vector *vec* de 16 bits.
- *values* corresponde al vector donde originalmente se guardaron los datos de las matrices ![[Pasted image 20211128214603.png]]
#### Evaluación experimental
- Se evalúa el tamaño de $vec$ para los datasets de 8x8, 128x128 y 512x512 elementos.
### 3.
- Se crea un sdsl::bit_vector $b$, donde se codificará un 1 cada vez que un nuevo elemento aparezca, y un 0 por cada repetición.
- Se crea un nuevo sdsl::int_vector de 16 bits $v$, en este vector se almacenaran los valores no repetidos de la secuencia original (que está en *vec*).
![[Pasted image 20211128215319.png]]
#### Evaluación experimental
- Se evalúa el tamaño de $b$ y $v$ para los datasets de 8x8, 128x128 y 512x512 elementos.
### 4.
- Se utiliza sdsl::rrr_vector, que fue el que menos espacio obtuvo luego de calcular manualmente el tamaño utilizando la complejidad entregada en el *cheat sheet* de la sdsl.
- Se utiliza una estructura rank para el rrr_vector.
- El índice de la secuencia original se puede calcular de la siguiente como $vec[i] = v[rrr\_rank(i)-1]$.
![[Pasted image 20211128220250.png]]
#### Evaluación experimental
- Se evalúa el tamaño de $rrr$ para los datasets de 8x8, 128x128 y 512x512 elementos.
- Se evalúa el tiempo de la opración $access$ al aplicar la operación de rank, versus la de acceder directamente en el int_vector $vec$.
### 5.
- Inicialmente cuando se leen los datos de los archivos de dataset, estos se almacenan en forma matricial en una matriz $M$ de 3 dimensiones, donde la primera dimensión representa el instante de tiempo $i$.
- Posteriormente se crea un arreglo de vector de vector$<int>$ $BM$, formado a partir de la matriz $M$, donde cada posición de $BM[i]$ es 1 si esa misma posición en $M_{i-1}$ es distinta a la posición en $M_i$, o 0 en caso contrario.
- Se crea un vector de sdsl::k2_tree $k2ts$, donde cada posición del vector representa un k2tree para el instante de tiempo $i$.
- Se hace uso del contructor del k2tree que recibe un $vector<vector<int>>$, se hace esto por cada posición del vector donde se contruye en base a $BM_i$.
![[Pasted image 20211128222101.png]]
#### Evaluación experimental
- Se evalúa el tamaño de $M$, $BM$ y $k2ts$ para los datasets de 8x8, 128x128 y 512x512 elementos.
### 6.
- Para representar las diferencias de las matrices de manera compacta, al igual que en la actividad 3 se hace uso de un int_vector $v$ y un bit_vector $b$.
- Se recorren todas la matrices posición por posición, se calcula la diferencia de la posición actual entre la matriz $M_i-1$ y $M_i$, $diff$.
- Si $diff$ es un valor nuevo, se almacena en $v$, y en $b$ se almacena un 1. 
- Si $diff$ es igual al de la posición anterior, en $v$ no se guarda nada, en $b$ se almacena un 0.
- Dado que sdsl::int_vector no soporta números negativos, una forma de solucionar el problema de mostrar los valores originales, es castearlo a int de 64 bits con $(int64\_t)v[i]$.
![[Pasted image 20211128231154.png]]