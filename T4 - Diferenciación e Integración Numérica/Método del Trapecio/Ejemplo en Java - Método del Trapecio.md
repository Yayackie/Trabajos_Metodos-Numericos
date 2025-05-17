# Tema 4: Método del Trapecio - Ejemplo en Java con salida esperada
## Método del Trapecio
```java
public class TrapezoidalRule {
    public static double f(double x) {
        return Math.exp(x);
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        int n = 4;

        double h = (b - a) / n;
        double suma = f(a) + f(b);

        for (int i = 1; i < n; i++) {
            double x = a + i * h;
            suma += 2 * f(x);
        }

        double integral = (h / 2) * suma;
        System.out.printf("Integral aproximada: %.3f%n", integral);
    }
}
```
**Salida Esperada**
```markdown
Integral aproximada: 1.721
```
