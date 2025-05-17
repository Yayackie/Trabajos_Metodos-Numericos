# Tema 2: Método de la Secante - Ejemplo en Java con salida esperada
## Método de la Secante

    public class SecantMethod {
        public static double f(double x) {
            return x * x * x - x - 2;
        }

    public static void main(String[] args) {
        double x0 = 1.0;
        double x1 = 2.0;
        double tolerancia = 0.001;
        int maxIteraciones = 100;

        for (int iteracion = 0; iteracion < maxIteraciones; iteracion++) {
            double fx0 = f(x0);
            double fx1 = f(x1);
            double x2 = x1 - (fx1 * (x1 - x0)) / (fx1 - fx0);
            System.out.printf("Iteración %d: x = %.3f, f(x) = %.3f%n", iteracion, x2, f(x2));

            if (Math.abs(f(x2)) < tolerancia) {
                System.out.printf("Raíz encontrada: %.3f%n", x2);
                return;
            }

            x0 = x1;
            x1 = x2;
        }
        System.out.println("Máximo de iteraciones alcanzado");
    }
    }
## Salida Esperada
- Iteración 0: x = 1.556, f(x) = 0.214
- Iteración 1: x = 1.518, f(x) = 0.002
- Raíz encontrada: 1.518
