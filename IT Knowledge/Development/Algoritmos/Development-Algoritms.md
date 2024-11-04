---
creation Date: 2024-10-29 13:52
last modification: " 2024-10-29 13:52"
folder: Algoritmos
aliases: 
tags:
---
___
**Relacionado**

[[Hub-Development]]

---
**Tabla de contenidos**

- [[#Orígenes|Orígenes]]
- [[#Definición|Definición]]
	- [[#Definición#Como definir un algoritmo:|Como definir un algoritmo:]]

___
## Orígenes
- La palabra "algoritmo" proviene del nombre del matemático persa **Al-Juarismi**, que escribió sobre aritmética y álgebra en el siglo IX.
    - Los algoritmos han existido en diversas formas desde la antigüedad, en contextos como la geometría y la aritmética.
    
	- ### **Evolución**:
	    - Con el desarrollo de las computadoras en el siglo XX, el concepto de algoritmo se formalizó y se convirtió en un elemento fundamental en la programación.
	    - Algoritmos como la búsqueda y ordenación se volvieron esenciales a medida que se necesitaban resolver problemas complejos en computación.
    
	- ### **Lenguajes de Programación**:
	    - Los algoritmos son independientes del lenguaje, pero algunos lenguajes están diseñados para facilitar ciertos tipos de algoritmos:
	        - **Python**: Popular en el ámbito académico y en la ciencia de datos por su sintaxis sencilla.
	        - **C/C++**: Utilizados en sistemas embebidos y para algoritmos de alto rendimiento.
	        - **Java**: Común en aplicaciones empresariales y en sistemas donde la portabilidad es importante.

## Definición
- Un algoritmo en una secuencia estructurada de pasos para resolver un problema.
### Como definir un algoritmo:
1. Este debe definir claramente el problema, sus entradas y salidas.
2. Sus  pasos deben seguir un orden especifico.
3. Debe producir un resultado
4. Debe completarse en un tiempo finito.
### Corrección y eficiencia
- Antes de evaluar un algoritmo por eficiencia debemos asegurar su corrección.
- Antes de definir un algoritmo empezamos definiendo el problema, en el problema se especifica las entradas y salidas.
- Un algoritmo se considera exitosos si cada ejecución del algoritmo con todo valor posible de entrada obtenemos el resultado esperado
#### Corrección
- Para cualquier posible entrada al algoritmo, este debe terminar o encontrar el valor buscado.
- La corrección de un algoritmo se demuestra mediante ==induccion matematica==, esto implica escribir una especificación y prueba de corrección.
### Eficiencia
#### Medición en tiempo y espacio.
- Running time
- Time complexity
- Space complexity
- Growth Rate - Order of Growth
#### Big O Notation
- Definición teórica de la complejidad de un algoritmo en función a su tamaño.

1. **O(1)** - Complejidad constante:
	- El tiempo de ejecución no cambia con el tamaño de los datos.
	- Caso ideal respecto al Runtime.
1. **O(log n)** - Complejidad logarítmica: El tiempo de ejecución crece logarítmicamente en relación con el tamaño de los datos.
2. **O(n)** - Complejidad lineal: El tiempo de ejecución crece linealmente con el tamaño de los datos.
3. **O(n log n)** - Complejidad lineal-logarítmica: Típicamente ocurre en algoritmos de ordenación eficientes.
4. **O(n²)** - Complejidad cuadrática: El tiempo de ejecución crece cuadráticamente con el tamaño de los datos.
5. **O(2^n)** - Complejidad exponencial: El tiempo de ejecución se duplica con cada incremento en el tamaño de los datos.
#### Algoritmos
##### 1. Busqueda Lineal
O(1) - Complejidad lineal
##### 2. Busqueda Binaria
O(log n) - Complejidad logaritmica