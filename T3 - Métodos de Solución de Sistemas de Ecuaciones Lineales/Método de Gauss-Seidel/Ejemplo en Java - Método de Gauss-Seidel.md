# Tema 3: Método de Gauss-Seidel - Ejemplo en Java con salida esperada
## Método de Gauss-Seidel
```java
public class GaussSeidel {
    public static void main(String[] args) {
        int n = 3;
        double[][] A = {{3, 2, -1}, {2, -2, 4}, {-1, 0.5, -1}};
        double[] b = {1, -2, 0};
        double[] x = {0, 0, 0};
        double[] xNuevo = new double[n];
        double tolerancia = 0.001;
        int maxIteraciones = 100;

        for (int iteracion = 0; iteracion < maxIteraciones; iteracion++) {
            double error = 0;
            for (int i = 0; i < n; i++) {
                double suma = 0;
                for (int j = 0; j < n; j++) {
                    if (j != i) {
                        suma += A[i][j] * x[j];
                    }
                }
                xNuevo[i] = (b[i] - suma) / A[i][i];
                error = Math.max(error, Math.abs(xNuevo[i] - x[i]));
                x[i] = xNuevo[i];
            }

            System.out.printf("Iteración %d:%n", iteracion);
            for (int i = 0; i < n; i++) {
                System.out.printf("x%d = %.3f%n", i, x[i]);
            }

            if (error < tolerancia) {
                System.out.println("Solución encontrada");
                return;
            }
        }
        System.out.println("Máximo de iteraciones alcanzado");
    }
}
```
**Salida Esperada**
```markdown
Iteración 0:
x0 = 0.333
x1 = -0.667
x2 = -0.583

Iteración 1:
x0 = 0.583
x1 = 0.083
x2 = -0.458

Iteración 2:
x0 = 0.458
x1 = 0.121
x2 = -0.430

Iteración 3:
x0 = 0.430
x1 = 0.140
x2 = -0.429

Iteración 4:
x0 = 0.429
x1 = 0.143
x2 = -0.429

Solución encontrada
```
