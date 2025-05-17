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
- Iteración 1: x = 1.521, f(x) = 0.001
- Raíz encontrada: 1.521
