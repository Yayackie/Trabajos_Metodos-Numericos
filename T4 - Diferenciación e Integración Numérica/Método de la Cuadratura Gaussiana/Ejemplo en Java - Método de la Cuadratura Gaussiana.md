# Tema 4: Método de la Cuadratura Gaussiana - Ejemplo en Java con salida esperada
## Método de la Cuadratura Gaussiana
```java
public class GaussianQuadrature {
    public static double f(double x) {
        return Math.exp(x);
    }

    public static void main(String[] args) {
        double a = 0.0;
        double b = 1.0;
        int n = 3;
        double[] puntos = {-0.774596669, 0.0, 0.774596669};
        double[] pesos = {0.555555556, 0.888888889, 0.555555556};

        double suma = 0;
        for (int i = 0; i < n; i++) {
            double t = puntos[i];
            double x = ((b - a) * t + (b + a)) / 2;
            suma += pesos[i] * f(x);
        }

        double integral = ((b - a) / 2) * suma;
        System.out.printf("Integral aproximada: %.3f%n", integral);
    }
}
```
**Salida Esperada**
```markdown
Integral aproximada: 1.718
```
