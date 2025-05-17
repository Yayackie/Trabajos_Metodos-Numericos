# Tema 2: Tipos de Errores Numéricos
## Error de Redondeo

### ¿Qué es?

El error de redondeo es uno de los errores más comunes en los métodos numéricos y se origina en la representación limitada de los números reales dentro de un sistema digital. Las computadoras utilizan un número finito de bits para representar números, lo que significa que muchos valores decimales no pueden almacenarse exactamente y deben redondearse al número más cercano que pueda ser representado. Este proceso introduce una pequeña discrepancia entre el valor real y su representación computacional.

Aunque un solo error de redondeo puede parecer insignificante, su efecto se vuelve crítico cuando se realizan muchas operaciones aritméticas consecutivas. Las sumas, multiplicaciones, divisiones o funciones más complejas pueden propagar y amplificar estos errores, afectando la precisión final. Por esta razón, es esencial diseñar algoritmos estables que minimicen su acumulación.

