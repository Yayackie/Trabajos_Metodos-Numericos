# Tema 5: Interpolación Polinómica - Ejemplo en Java con salida esperada
## Interpolación Polinómica
```java
public class PolynomialInterpolation {
    public static void main(String[] args) {
        double[] x = {0, 1, 2, 3};
        double[] y = {1, 2.718, 7.389, 20.085};
        double xp = 1.5;
        int n = x.length;
        double yp = 0;

        for (int i = 0; i < n; i++) {
            double L = 1;
            for (int j = 0; j < n; j++) {
                if (j != i) {
                    L *= (xp - x[j]) / (x[i] - x[j]);
                }
            }
            yp += y[i] * L;
        }

        System.out.printf("Valor interpolado en x = %.1f: %.3f%n", xp, yp);
    }
}
```
**Salida Esperada**
```markdown
Valor interpolado en x = 1.5: 4.482
```
