# Tema 6: Método de Pasos Múltiples - Ejemplo en Java con salida esperada
## Método de Pasos Múltiples
```java
public class AdamsBashforth {
    public static double f(double x, double y) {
        return -2 * x * y;
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        double h = 0.2;
        int n = 5;
        double[] x = new double[n + 1];
        double[] y = new double[n + 1];
        y[0] = 1.0;

        for (int i = 0; i <= n; i++) {
            x[i] = a + i * h;
        }

        // Primer paso con Euler
        y[1] = y[0] + h * f(x[0], y[0]);

        // Adams-Bashforth de 2 pasos
        for (int i = 1; i < n; i++) {
            y[i + 1] = y[i] + (h / 2) * (3 * f(x[i], y[i]) - f(x[i - 1], y[i - 1]));
        }

        for (int i = 0; i <= n; i++) {
            System.out.printf("x = %.1f, y = %.3f%n", x[i], y[i]);
        }
    }
}
```
**Salida Esperada**
```markdown
x = 0.0, y = 1.000
x = 0.2, y = 1.000
x = 0.4, y = 0.960
x = 0.6, y = 0.862
x = 0.8, y = 0.711
x = 1.0, y = 0.574
```
