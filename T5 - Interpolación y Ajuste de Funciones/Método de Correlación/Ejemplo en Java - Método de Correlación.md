# Tema 5: Método de Correlación - Ejemplo en Java con salida esperada
## Método de Correlación
```java
public class Correlation {
    public static void main(String[] args) {
        double[] x = {0, 1, 2, 3};
        double[] y = {1, 2.718, 7.389, 20.085};
        int n = x.length;
        double sumX = 0, sumY = 0, sumXY = 0, sumX2 = 0, sumY2 = 0;

        for (int i = 0; i < n; i++) {
            sumX += x[i];
            sumY += y[i];
            sumXY += x[i] * y[i];
            sumX2 += x[i] * x[i];
            sumY2 += y[i] * y[i];
        }

        double r = (n * sumXY - sumX * sumY) / 
                   Math.sqrt((n * sumX2 - sumX * sumX) * (n * sumY2 - sumY * sumY));

        System.out.printf("Coeficiente de correlación: %.3f%n", r);
    }
}
```
**Salida Esperada**
```markdown
Coeficiente de correlación: 0.904
```
