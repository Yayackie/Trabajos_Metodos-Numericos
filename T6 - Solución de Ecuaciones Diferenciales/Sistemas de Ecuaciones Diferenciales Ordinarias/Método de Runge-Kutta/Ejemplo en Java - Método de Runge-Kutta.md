# Tema 6: Método de Runge-Kutta - Ejemplo en Java con salida esperada
## Método de Runge-Kutta
```java
public class RungeKutta {
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
            double k1 = f(x[i], y[i]);
            double k2 = f(x[i] + h/2, y[i] + (h/2) * k1);
            double k3 = f(x[i] + h/2, y[i] + (h/2) * k2);
            double k4 = f(x[i] + h, y[i] + h * k3);
            y[i + 1] = y[i] + (h / 6) * (k1 + 2 * k2 + 2 * k3 + k4);
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
x = 0.2, y = 0.961
x = 0.4, y = 0.852
x = 0.6, y = 0.697
x = 0.8, y = 0.527
x = 1.0, y = 0.368
```
