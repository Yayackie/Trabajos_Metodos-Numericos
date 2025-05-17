# Método de un paso
## Introducción
Los métodos de un paso constituyen una clase fundamental de técnicas numéricas para resolver ecuaciones diferenciales ordinarias. Su característica principal es que el valor de la solución en el siguiente punto depende únicamente del valor en el punto actual. Es decir, no requieren almacenar o utilizar información de pasos anteriores, lo que los hace simples de implementar y controlar.

Un ejemplo clásico de este enfoque es el método de Euler, que utiliza una aproximación lineal basada en la derivada de la función para avanzar de un punto al siguiente. También se incluyen aquí variantes más precisas como el método de Heun y el método de Runge-Kutta. Estos métodos mejoran la precisión del método de Euler al considerar evaluaciones adicionales de la función derivada dentro del mismo paso.

Aunque los métodos de un paso son conceptualmente simples y adecuados para una amplia gama de problemas, pueden requerir pasos pequeños para mantener la estabilidad y precisión, especialmente en ecuaciones rígidas. Aun así, siguen siendo herramientas muy poderosas y son la base de muchos algoritmos más complejos en el análisis numérico.


