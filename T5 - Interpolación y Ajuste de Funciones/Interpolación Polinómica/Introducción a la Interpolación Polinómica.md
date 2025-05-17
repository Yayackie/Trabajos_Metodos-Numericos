# Interpolación Polinómica
## Introducción
La interpolación polinómica busca construir un polinomio de grado n + 1 puntos conocidos. A diferencia de la interpolación lineal, este método puede capturar mejor la curvatura y complejidad de una función subyacente, ya que emplea expresiones matemáticas más ricas en términos de comportamiento.

Entre los métodos más utilizados dentro de la interpolación polinómica se encuentran la interpolación de Newton y la de Lagrange. Ambos permiten construir el polinomio que representa los datos, pero utilizan distintas formulaciones para hacerlo. Estos métodos se consideran exactos para los puntos conocidos, pero pueden presentar problemas de oscilación (conocido como fenómeno de Runge) cuando se utilizan polinomios de alto grado en intervalos amplios.

La interpolación polinómica es especialmente valiosa cuando se tiene un número moderado de datos distribuidos uniformemente y se busca una función que se adapte con exactitud. Sin embargo, en aplicaciones con muchos datos, suelen preferirse métodos alternativos como los splines o el ajuste de funciones, para evitar inestabilidad numérica.
