# Tema 4: Método de Simpson 3/8 - Ejemplo en Java con salida esperada
## Método de Simpson 3/8
```java
public class SimpsonThreeEighths {
    public static double f(double x) {
        return Math.exp(x);
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        int n = 3;

        if (n % 3 != 0) {
            System.out.println("El número de subintervalos debe ser múltiplo de 3");
            return;
        }

        double h = (b - a) / n;
        double suma = f(a) + f(b);

        for (int i = 1; i < n; i++) {
            double x = a + i * h;
            if (i % 3 == 0) {
                suma += 2 * f(x);
            } else {
                suma += 3 * f(x);
            }
        }

        double integral = (3 * h / 8) * suma;
        System.out.printf("Integral aproximada: %.3f%n", integral);
    }
}
```
**Salida Esperada**
```markdown
Integral aproximada: 1.718
```
