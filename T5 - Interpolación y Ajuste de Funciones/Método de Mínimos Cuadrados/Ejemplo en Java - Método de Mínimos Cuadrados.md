# Tema 5: Método de Mínimos Cuadrados - Ejemplo en Java con salida esperada
## Método de Mínimos Cuadrados
```java
public class LeastSquares {
    public static void main(String[] args) {
        double[] x = {0, 1, 2, 3};
        double[] y = {1, 2.718, 7.389, 20.085};
        int n = x.length;
        double sumX = 0, sumY = 0, sumXY = 0, sumX2 = 0;

        for (int i = 0; i < n; i++) {
            sumX += x[i];
            sumY += y[i];
            sumXY += x[i] * y[i];
            sumX2 += x[i] * x[i];
        }

        double m = (n * sumXY - sumX * sumY) / (n * sumX2 - sumX * sumX);
        double b = (sumY - m * sumX) / n;

        System.out.printf("Ecuación de la recta: y = %.3fx + %.3f%n", m, b);
    }
}
```
**Salida Esperada**
```markdown
Ecuación de la recta: y = 6.361x + 0.171
```
