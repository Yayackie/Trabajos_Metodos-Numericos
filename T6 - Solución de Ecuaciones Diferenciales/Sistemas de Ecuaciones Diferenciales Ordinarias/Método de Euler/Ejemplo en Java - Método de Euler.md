# Tema 6: Método de Euler - Ejemplo en Java con salida esperada
## Método de Euler
```java
public class EulerMethod {
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

        for (int i = 0; i < n; i++) {
            y[i + 1] = y[i] + h * f(x[i], y[i]);
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
x = 0.6, y = 0.846
x = 0.8, y = 0.677
x = 1.0, y = 0.488
```
