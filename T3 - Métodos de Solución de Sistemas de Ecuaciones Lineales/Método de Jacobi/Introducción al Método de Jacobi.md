# Método de Jacobi
## Introducción al Método de Jacobi
El método de Jacobi es otro método iterativo utilizado para resolver sistemas de ecuaciones lineales. A diferencia del método de Gauss-Seidel, el método de Jacobi calcula las nuevas aproximaciones de todas las variables utilizando únicamente los valores de la iteración anterior, sin actualizarlos en el mismo ciclo. Esta independencia lo convierte en un método sencillo de paralelizar, lo que es útil en aplicaciones de cómputo paralelo.

El algoritmo es simple y fácil de implementar, y puede aplicarse a sistemas con estructuras dispersas. Al igual que Gauss-Seidel, requiere que el sistema cumpla ciertas condiciones para garantizar la convergencia, como la dominancia diagonal. Sin embargo, suele converger más lentamente que Gauss-Seidel en la práctica.

A pesar de ser menos eficiente que otros métodos iterativos en muchos casos, el método de Jacobi sigue siendo relevante como base para el estudio de técnicas numéricas iterativas, y también es útil en contextos donde el paralelismo o la independencia entre procesos es esencial para el rendimiento computacional.


