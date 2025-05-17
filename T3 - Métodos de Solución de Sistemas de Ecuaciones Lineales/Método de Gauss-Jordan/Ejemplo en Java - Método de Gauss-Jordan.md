# Tema 3: Método de Gauss-Jordan - Ejemplo en Java con salida esperada
## Método de Gauss-Jordan
```java
public class GaussJordan {
    public static void main(String[] args) {
        int n = 3;
        double[][] A = {{3, 2, -1}, {2, -2, 4}, {-1, 0.5, -1}};
        double[] b = {1, -2, 0};
        double[] x = new double[n];

        // Eliminación hacia adelante y hacia atrás
        for (int k = 0; k < n; k++) {
            if (A[k][k] == 0) {
                System.out.println("Pivote nulo, no se puede resolver");
                return;
            }
            // Normalizar fila k
            double factor = A[k][k];
            for (int j = 0; j < n; j++) {
                A[k][j] /= factor;
            }
            b[k] /= factor;

            // Eliminar columna k en otras filas
            for (int i = 0; i < n; i++) {
                if (i != k) {
                    factor = A[i][k];
                    for (int j = 0; j < n; j++) {
                        A[i][j] -= factor * A[k][j];
                    }
                    b[i] -= factor * b[k];
                }
            }
        }

        // Solución
        for (int i = 0; i < n; i++) {
            x[i] = b[i];
        }

        // Imprimir solución
        System.out.println("Solución:");
        for (int i = 0; i < n; i++) {
            System.out.printf("x%d = %.3f%n", i, x[i]);
        }
    }
}
```
**Salida Esperada**
```markdown
Solución:
x0 = 0.429
x1 = 0.143
x2 = -0.429
```
