# Tema 1: Error de Truncamiento - Ejemplo en Java con salida esperada

## Error de Truncamiento
    public class ErrorTruncamiento {
        public static double taylorExp(double x, int n) {
            double suma = 1.0;
            double term = 1.0;
    
            for (int i = 1; i <= n; i++) {
                term *= x / i;
                suma += term;
            }
    
            return suma;
        }
    
        public static void main(String[] args) {
            double x = 1.0;
            int n = 3;
    
            double real = Math.exp(x);
            double aproximado = taylorExp(x, n);
    
            System.out.printf("Valor real: %.3f%n", real);
            System.out.printf("Aproximación (n=3): %.3f%n", aproximado);
            System.out.printf("Error de truncamiento: %.3f%n", Math.abs(real - aproximado));
        }
    }

### Salida esperada del código:
    Valor real: 2.718  
    Aproximación (n=3): 2.667  
    Error de truncamiento: 0.051  
    
