# Método de Gauss-Jordan
## Introducción al Método de Gauss-Jordan
El método de Gauss-Jordan es una extensión del método de eliminación gaussiana, que va un paso más allá al transformar la matriz aumentada del sistema no solo a una forma escalonada, sino a una forma reducida por filas (también conocida como forma canónica). Esto significa que no solo se busca ceros debajo de la diagonal principal, sino también encima de ella, dejando una matriz diagonal o una matriz identidad en el caso de sistemas con solución única.

Este método permite obtener directamente la solución del sistema sin necesidad de aplicar la sustitución regresiva, lo cual lo hace más directo. Además, resulta particularmente útil cuando se desea invertir una matriz o resolver múltiples sistemas con la misma matriz de coeficientes, ya que su algoritmo transforma la matriz completa.

A pesar de su precisión y generalidad, el método de Gauss-Jordan tiene un costo computacional mayor que el de la eliminación gaussiana. Su complejidad lo vuelve poco práctico para sistemas de gran tamaño, donde los métodos iterativos o variantes optimizadas resultan más eficientes. No obstante, es una excelente herramienta didáctica y útil para comprender en profundidad la naturaleza algebraica de los sistemas lineales.


