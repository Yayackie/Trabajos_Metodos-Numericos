# Tema 4: Método de Simpson 1/3 - Ejemplo en Java con salida esperada
## Método de Simpson 1/3
```java
public class SimpsonOneThird {
    public static double f(double x) {
        return Math.exp(x);
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        int n = 4;

        if (n % 2 != 0) {
            System.out.println("El número de subintervalos debe ser par");
            return;
        }

        double h = (b - a) / n;
        double suma = f(a) + f(b);

        for (int i = 1; i < n; i++) {
            double x = a + i * h;
            if (i % 2 == 0) {
                suma += 2 * f(x);
            } else {
                suma += 4 * f(x);
            }
        }

        double integral = (h / 3) * suma;
        System.out.printf("Integral aproximada: %.3f%n", integral);
    }
}
```
**Salida Esperada**
```markdown
Integral aproximada: 1.718
```
