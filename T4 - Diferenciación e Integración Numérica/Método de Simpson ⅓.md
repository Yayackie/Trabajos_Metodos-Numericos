# Tema 4: Método de Simpson 1/3

## Introducción

El método de Simpson 1/3 es una técnica de integración numérica que permite aproximar el valor de una integral definida a partir de una combinación de valores de la función evaluados en puntos igualmente espaciados. Este método es particularmente útil cuando se tiene una función continua y suave dentro del intervalo de integración, y se basa en aproximar el área bajo la curva mediante parábolas.

El fundamento del método radica en utilizar polinomios de segundo grado para estimar la función dentro de subintervalos. Para aplicar esta técnica, el intervalo de integración se divide en un número par de segmentos (es decir, un número impar de puntos), y se utiliza una fórmula específica que pondera los extremos y los puntos medios del intervalo. Esta fórmula proporciona una mayor precisión que la del método del trapecio, especialmente si la función se comporta de manera suave.

Gracias a su simplicidad y precisión, el método de Simpson 1/3 es ampliamente usado en aplicaciones de ingeniería, física y ciencias aplicadas. No obstante, su correcta implementación requiere que se cumplan ciertas condiciones, como el número par de subintervalos, y puede perder precisión si la función presenta muchos cambios bruscos o discontinuidades dentro del intervalo.

---

### Ventajas y Desventajas

**Ventajas:**
- Ofrece mayor precisión que el método del trapecio al usar parábolas para la aproximación.
- Es relativamente simple de implementar y eficiente para funciones suaves.
- Proporciona buenos resultados con un número moderado de subintervalos.

**Desventajas:**
- Requiere un número par de subintervalos para su aplicación.
- Pierde precisión si la función tiene discontinuidades o cambios bruscos.
- No es adecuado para funciones con alta oscilación o singularidades dentro del intervalo.

---

### Pseudocódigo

```text
Inicio
  Función f(x)
    Retornar exp(x)
  Fin Función

  Definir a como real
  Definir b como real
  Definir n como entero
  Definir h como real
  Definir suma como real
  Definir x como real
  Definir i como entero
  Definir integral como real

  a = 0.0
  b = 1.0
  n = 4

  Si n mod 2 != 0
    Imprimir "El número de subintervalos debe ser par"
    Retornar
  Fin Si

  h = (b - a) / n
  suma = f(a) + f(b)

  Para i = 1 hasta n-1
    x = a + i * h
    Si i mod 2 = 0
      suma = suma + 2 * f(x)
    Sino
      suma = suma + 4 * f(x)
    Fin Si
  Fin Para

  integral = (h / 3) * suma
  Imprimir "Integral aproximada: ", integral
Fin
```

### Código base en Java

```java
public class CodigoBaseSimpsonOneThird {
    public static double f(double x) {
        return Math.exp(x);
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        int n = 4;

        if (n % 2 != 0) {
            System.out.println("El número de subintervalos debe ser par");
            return;
        }

        double h = (b - a) / n;
        double suma = f(a) + f(b);

        for (int i = 1; i < n; i++) {
            double x = a + i * h;
            if (i % 2 == 0) {
                suma += 2 * f(x);
            } else {
                suma += 4 * f(x);
            }
        }

        double integral = (h / 3) * suma;
        System.out.println("Integral aproximada: " + integral);
    }
}
```

### Ejemplo funcional en Java

```java
public class SimpsonOneThird {
    public static double f(double x) {
        return Math.exp(x);
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        int n = 4;

        if (n % 2 != 0) {
            System.out.println("El número de subintervalos debe ser par");
            return;
        }

        double h = (b - a) / n;
        double suma = f(a) + f(b);

        for (int i = 1; i < n; i++) {
            double x = a + i * h;
            if (i % 2 == 0) {
                suma += 2 * f(x);
            } else {
                suma += 4 * f(x);
            }
        }

        double integral = (h / 3) * suma;
        System.out.printf("Integral aproximada: %.3f%n", integral);
    }
}
```

### Caso de prueba:

```text
Integral aproximada: 1.718
```
### [<- T4 - Diferenciación e Integración Numérica ](https://github.com/Yayackie/Trabajos_Metodos-Numericos/blob/main/T4%20-%20Diferenciaci%C3%B3n%20e%20Integraci%C3%B3n%20Num%C3%A9rica/Introducci%C3%B3n%20a%20la%20DIferenciai%C3%B3n%20e%20Integraci%C3%B3n%20Num%C3%A9rica.md)
