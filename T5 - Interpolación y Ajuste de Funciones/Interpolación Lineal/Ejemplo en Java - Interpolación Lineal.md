# Tema 5: Interpolación Lineal - Ejemplo en Java con salida esperada
## Interpolación Lineal
```java
public class LinearInterpolation {
    public static void main(String[] args) {
        double[] x = {0, 1, 2, 3};
        double[] y = {1, 2.718, 7.389, 20.085};
        double xp = 1.5;
        int n = x.length;

        for (int i = 0; i < n - 1; i++) {
            if (x[i] <= xp && xp <= x[i + 1]) {
                double yp = y[i] + (y[i + 1] - y[i]) * (xp - x[i]) / (x[i + 1] - x[i]);
                System.out.printf("Valor interpolado en x = %.1f: %.3f%n", xp, yp);
                return;
            }
        }
        System.out.println("Punto fuera del rango de interpolación");
    }
}
```
**Salida Esperada**
```markdown
Valor interpolado en x = 1.5: 5.054
```
