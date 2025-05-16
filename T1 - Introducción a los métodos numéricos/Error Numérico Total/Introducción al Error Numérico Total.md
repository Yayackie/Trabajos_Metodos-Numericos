# Tema 2: Tipos de Errores Numéricos

## ¿De qué trata?

Este tema aborda los distintos tipos de errores que pueden surgir al aplicar métodos numéricos. Estos errores son inevitables debido a las limitaciones de las representaciones numéricas en las computadoras, las simplificaciones matemáticas y otros factores tanto humanos como estructurales. Entender su origen y comportamiento es fundamental para interpretar correctamente los resultados numéricos y mejorar la estabilidad y precisión de los algoritmos utilizados.

A lo largo de esta sección, exploraremos en detalle el error de redondeo, error de truncamiento, error numérico total, errores por equivocación, errores de formulación, incertidumbre en los datos y error por cancelación numérica. Cada uno de estos errores representa un componente clave en la calidad final de los resultados numéricos y en la toma de decisiones computacionales.

---

## Error de Redondeo

### ¿Qué es?

El error de redondeo es uno de los errores más comunes en los métodos numéricos y se origina en la representación limitada de los números reales dentro de un sistema digital. Las computadoras utilizan un número finito de bits para representar números, lo que significa que muchos valores decimales no pueden almacenarse exactamente y deben redondearse al número más cercano que pueda ser representado. Este proceso introduce una pequeña discrepancia entre el valor real y su representación computacional.

Aunque un solo error de redondeo puede parecer insignificante, su efecto se vuelve crítico cuando se realizan muchas operaciones aritméticas consecutivas. Las sumas, multiplicaciones, divisiones o funciones más complejas pueden propagar y amplificar estos errores, afectando la precisión final. Por esta razón, es esencial diseñar algoritmos estables que minimicen su acumulación.

---

## Error de Truncamiento

### ¿Qué es?

El error de truncamiento se produce cuando se interrumpe o se simplifica una operación matemática infinita o continua para poder ser calculada de forma finita. Por ejemplo, al utilizar una serie de Taylor para aproximar funciones, es necesario cortar la serie después de un número determinado de términos, lo que introduce un error al omitir los términos restantes.

La magnitud del error de truncamiento depende del número de términos o pasos utilizados en la aproximación: a mayor cantidad de términos considerados, menor será el error, pero mayor será el costo computacional. Existe un compromiso entre precisión y eficiencia que debe ser evaluado según el problema específico.

---

## Error Numérico Total

### ¿Qué es?

El error numérico total es la combinación de todos los errores que pueden surgir en un cálculo numérico. Representa la diferencia neta entre el valor exacto teórico de una cantidad y el valor obtenido mediante una aproximación. Este error engloba errores de redondeo, truncamiento, errores del modelo matemático e incluso errores por cancelación o incertidumbre en los datos de entrada.

Comprender el error numérico total es fundamental para evaluar la confiabilidad de los resultados obtenidos con métodos numéricos. Este análisis permite decidir qué método aplicar, cuántas iteraciones realizar o cuánta precisión es necesaria en los datos iniciales para obtener un resultado aceptable.

---

## Errores por Equivocación

### ¿Qué es?

Los errores por equivocación, también conocidos como errores humanos, ocurren cuando se comete una falla durante la formulación, programación o ejecución de un método numérico. Estos pueden incluir errores al ingresar datos, escribir una fórmula incorrecta, seleccionar mal el método para resolver un problema o malinterpretar los resultados obtenidos.

Aunque no son inherentes al método numérico en sí, su impacto puede ser significativo. La buena práctica en la implementación de algoritmos incluye la validación de resultados, revisión cruzada de código y verificación de entradas y salidas para minimizar estos errores.

---

## Errores de Formulación

### ¿Qué es?

Los errores de formulación se producen cuando el modelo matemático utilizado para describir un problema real es incorrecto o incompleto. Para facilitar el análisis y resolver problemas complejos, muchas veces se hacen simplificaciones o suposiciones que alejan el modelo de la realidad. Esto introduce un error que no proviene del método numérico, sino de una mala representación del fenómeno original.

Estos errores son especialmente peligrosos porque pueden pasar desapercibidos si el modelo parece funcionar correctamente bajo ciertas condiciones. Una formulación incorrecta puede invalidar completamente los resultados, sin importar qué tan preciso sea el método empleado.

---

## Incertidumbre en los Datos

### ¿Qué es?

En muchos problemas reales, los datos de entrada no se conocen con exactitud absoluta. Esta incertidumbre puede deberse a limitaciones en la medición, ruido experimental, redondeo de valores o estimaciones subjetivas. Como consecuencia, incluso si se utiliza un método numérico exacto, los resultados pueden estar afectados por el error presente en los datos iniciales.

La propagación de esta incertidumbre puede generar errores significativos en el resultado final, especialmente si el problema es sensible a pequeñas variaciones en los datos (mal condicionado). Por ello, se recomienda realizar análisis de sensibilidad y estimaciones de error para comprender su impacto.

---

## Error por Cancelación Numérica

### ¿Qué es?

La cancelación numérica ocurre cuando se restan dos números que son muy cercanos entre sí, lo que provoca una pérdida significativa de cifras significativas. Esta pérdida de precisión puede resultar en errores notables en cálculos posteriores, especialmente cuando los resultados intermedios se utilizan como base para otras operaciones.

Este tipo de error es muy común en ciertos algoritmos y fórmulas, por lo que se recomienda reescribir las expresiones algebraicas o utilizar formulaciones alternativas para evitar cancelaciones. Identificar y prevenir cancelaciones numéricas es clave para diseñar algoritmos estables y confiables.

