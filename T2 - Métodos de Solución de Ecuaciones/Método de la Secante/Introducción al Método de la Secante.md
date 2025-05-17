# Método de la Secante
## Introducción
El método de la secante es una técnica iterativa para encontrar raíces que busca mejorar la eficiencia del método de Newton-Raphson, eliminando la necesidad de calcular derivadas. A partir de dos valores iniciales, se genera una aproximación de la raíz trazando una línea recta entre los puntos evaluados de la función y encontrando su intersección con el eje horizontal. Este proceso se repite usando los dos valores más recientes.

Este enfoque tiene la ventaja de ser más rápido que métodos como la bisección y más práctico que Newton-Raphson cuando no se dispone de la derivada de la función. Sin embargo, es menos estable y puede divergir si los valores iniciales no están bien escogidos o si la función es muy irregular o no cumple ciertas condiciones.

El método de la secante es muy útil en situaciones donde la derivada es difícil de calcular o simplemente no está disponible. Aunque no siempre garantiza la convergencia, su simplicidad y eficiencia lo convierten en una opción atractiva en problemas reales donde se busca una solución rápida con bajo costo computacional.


