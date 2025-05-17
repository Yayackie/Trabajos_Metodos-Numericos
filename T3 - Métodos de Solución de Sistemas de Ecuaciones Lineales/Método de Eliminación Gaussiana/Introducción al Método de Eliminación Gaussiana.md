# Método de Eliminación Gaussiana
## Introducción al Método de Eliminación Gaussiana
El método de eliminación gaussiana es una técnica directa para resolver sistemas de ecuaciones lineales. Su objetivo principal es transformar el sistema original en una forma escalonada equivalente mediante operaciones elementales sobre las filas de la matriz aumentada. Estas operaciones incluyen el intercambio de filas, la multiplicación de una fila por un escalar distinto de cero y la suma o resta de filas. Una vez obtenida la forma escalonada, se puede aplicar el método de sustitución regresiva para hallar las soluciones del sistema.

Este método es ampliamente utilizado debido a su claridad conceptual y su aplicabilidad general. Es capaz de resolver cualquier sistema de ecuaciones lineales que tenga solución única, aunque también puede detectar sistemas inconsistentes o con infinitas soluciones si se aplica correctamente. La eliminación gaussiana es especialmente útil en sistemas pequeños o medianos, o cuando se necesita una solución exacta sin depender de iteraciones.

Sin embargo, su eficiencia disminuye considerablemente en sistemas muy grandes, ya que requiere una cantidad significativa de operaciones. Además, puede ser sensible a errores de redondeo en sistemas mal condicionados. Por esta razón, en entornos computacionales se suele acompañar de técnicas de pivoteo para mejorar la estabilidad numérica del método.


