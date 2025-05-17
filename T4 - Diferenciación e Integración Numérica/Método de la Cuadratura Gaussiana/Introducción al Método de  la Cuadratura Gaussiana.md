# Método de la Cuadratura Gaussiana
## Introducción
La cuadratura gaussiana es una técnica avanzada de integración numérica que permite obtener una alta precisión en la aproximación de integrales definidas con un número reducido de evaluaciones de la función. A diferencia de métodos como el del trapecio o Simpson, que utilizan puntos equidistantes en el intervalo de integración, la cuadratura gaussiana selecciona de forma óptima los puntos y pesos para minimizar el error.

El principio de este método se basa en calcular la integral como una suma ponderada de los valores de la función en ciertos puntos llamados "puntos de Gauss", los cuales no están distribuidos uniformemente. Estos puntos y sus respectivos pesos se obtienen a partir de los ceros de los polinomios ortogonales (como los de Legendre) sobre un intervalo específico. Esta propiedad permite que el método logre una precisión notable incluso usando pocos puntos de evaluación.

Gracias a su eficiencia y precisión, la cuadratura gaussiana es muy utilizada en problemas complejos donde se busca minimizar el costo computacional, como en simulaciones físicas, problemas de elementos finitos y cálculos científicos avanzados. No obstante, su implementación requiere mayor preparación que los métodos más básicos, ya que los puntos y pesos deben calcularse o consultarse previamente para cada número de nodos.


