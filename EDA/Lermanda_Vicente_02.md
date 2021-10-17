# Laboratorio 2
Profesor: Diego Seco N.
Ayudante: Alexander Irribara C.

## 1.
- Clase arreglo de sufijos.![[Pasted image 20211005194555.png|550]]
- Implementación de métodos de arreglo de sufijos: ![[Pasted image 20211005194736.png|550]]
- Pattern matching implementado en SA. Complejidad $O(mlog(n))$.![[Pasted image 20211005194811.png|550]]

## 2.
- Para el análisis experimental se utilizará un texto y un patrón creado con carácteres aleatorios del alfabeto en minúscula.
- Algoritmo de fuerza bruta utilizado $O(nm)$ donde $n$ es el largo del texto $T$, y $m$ el largo del patrón a buscar: ![[Pasted image 20211005200242.png|550]]
### a.
- Tamaño $n$ creciente (desde 1 a 10000) y patrones de largo aleatorio.![[Pasted image 20211005195645.png|550]]

<div style="page-break-after: always; visibility: hidden"> 
	\pagebreak 
</div>

#### Resultados
![[Pasted image 20211005223614.png|550]]
Según lo esperado y en base al análisis de peor caso, se observa que el algoritmo pattern matching implementado por el Suffix Array es bastante más eficiente que uno de fuerza bruta.


<div style="page-break-after: always; visibility: hidden"> 
	\pagebreak 
</div>

### b.
- Tamaño de $n$ fijo (100000) y diferentes tamaños de patrón $m$ (10000 ya que para 100000 tardaba más de 40 minutos y contando...).
#### Resultados
![[Pasted image 20211005233003.png]]
Dado que la complejidad de ambos algoritmos utilizados también dependen de $m$, es decir, el largo del patrón a buscar, el tiempo que tardan en ejecutarse aumenta, y según lo esperado, el SA hace esto de manera más eficiente que el acercamiento por fuerza bruta.
