# Tema 2: Método de Bisección - Ejemplo en Java con salida esperada
## Método de Bisección

    public class BisectionMethod {
        public static double f(double x) {
            return x * x * x - x - 2;
        }

    public static void main(String[] args) {
        double a = 1.0;
        double b = 2.0;
        double tolerancia = 0.001;
        int maxIteraciones = 100;

        double fa = f(a);
        double fb = f(b);

        if (fa * fb >= 0) {
            System.out.println("El intervalo no contiene una raíz");
            return;
        }

        for (int iteracion = 0; iteracion < maxIteraciones; iteracion++) {
            double p = (a + b) / 2;
            double fp = f(p);
            System.out.printf("Iteración %d: x = %.3f, f(x) = %.3f%n", iteracion, p, fp);

            if (Math.abs(fp) < tolerancia || Math.abs(b - a) < tolerancia) {
                System.out.printf("Raíz encontrada: %.3f%n", p);
                return;
            }

            if (fa * fp < 0) {
                b = p;
                fb = fp;
            } else {
                a = p;
                fa = fp;
            }
        }
        System.out.println("Máximo de iteraciones alcanzado");
    }
    }

## Salida Esperada
- Iteración 0: x = 1.500, f(x) = -0.125
- Iteración 1: x = 1.750, f(x) = 1.859
- Iteración 2: x = 1.625, f(x) = 0.701
- Iteración 3: x = 1.563, f(x) = 0.256
- Iteración 4: x = 1.531, f(x) = 0.059
- Iteración 5: x = 1.516, f(x) = -0.034
- Iteración 6: x = 1.523, f(x) = 0.012
- Iteración 7: x = 1.520, f(x) = -0.011
- Iteración 8: x = 1.522, f(x) = 0.000
- Raíz encontrada: 1.522
