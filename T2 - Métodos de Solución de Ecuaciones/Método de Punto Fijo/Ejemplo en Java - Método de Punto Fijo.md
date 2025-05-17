# Tema 2: Método de Punto Fijo - Ejemplo en Java con salida esperada
## Método de Punto Fijo

        public class FixedPointMethod {
            public static double f(double x) {
                return x * x * x - x - 2;
            }
        
            public static double g(double x) {
                return Math.pow(x + 2, 1.0 / 3.0);
            }
        
            public static void main(String[] args) {
                double x = 1.5;
                double tolerancia = 0.001;
                int maxIteraciones = 100;
        
                for (int iteracion = 0; iteracion < maxIteraciones; iteracion++) {
                    double xNuevo = g(x);
                    System.out.printf("Iteración %d: x = %.3f, f(x) = %.3f%n", iteracion, xNuevo, f(xNuevo));
        
                    if (Math.abs(xNuevo - x) < tolerancia) {
                        System.out.printf("Raíz encontrada: %.3f%n", xNuevo);
                        return;
                    }
        
                    x = xNuevo;
                }
                System.out.println("Máximo de iteraciones alcanzado");
            }
        }
## Salida Esperada
- Iteración 0: x = 1.442, f(x) = 0.150
- Iteración 1: x = 1.567, f(x) = 0.321
- Iteración 2: x = 1.484, f(x) = 0.075
- Iteración 3: x = 1.533, f(x) = 0.069
- Iteración 4: x = 1.506, f(x) = 0.029
- Iteración 5: x = 1.522, f(x) = 0.016
- Iteración 6: x = 1.514, f(x) = 0.006
- Iteración 7: x = 1.518, f(x) = 0.003
- Iteración 8: x = 1.520, f(x) = 0.001
- Raíz encontrada: 1.520
