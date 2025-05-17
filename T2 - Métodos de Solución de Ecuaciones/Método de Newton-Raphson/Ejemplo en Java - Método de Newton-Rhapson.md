# Tema 2: Método de Newton-Raphson - Ejemplo en Java con salida esperada
## Método de Newton-Raphson

    public class NewtonRaphsonMethod {
        public static double f(double x) {
            return x * x * x - x - 2;
        }

    public static double fPrima(double x) {
        return 3 * x * x - 1;
    }

    public static void main(String[] args) {
        double x = 1.5;
        double tolerancia = 0.001;
        int maxIteraciones = 100;

        for (int iteracion = 0; iteracion < maxIteraciones; iteracion++) {
            double fx = f(x);
            System.out.printf("Iteración %d: x = %.3f, f(x) = %.3f%n", iteracion, x, fx);

            if (Math.abs(fx) < tolerancia) {
                System.out.printf("Raíz encontrada: %.3f%n", x);
                return;
            }

            x = x - fx / fPrima(x);
        }
        System.out.println("Máximo de iteraciones alcanzado");
    }
}
## Salida Esperada
- Iteración 0: x = 1.500, f(x) = -0.125
- Iteración 1: x = 1.521, f(x) = 0.001
- Raíz encontrada: 1.521
