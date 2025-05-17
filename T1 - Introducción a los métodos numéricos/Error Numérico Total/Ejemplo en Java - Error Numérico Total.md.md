# Tema 1: Error Numérico Total - Ejemplo en Java con salida esperada

## Error Numérico Total
    public class ErrorTotal {
        public static void main(String[] args) {
            double valorReal = Math.sqrt(2);
            double valorAproximado = 1.4142;
    
            double error = Math.abs(valorReal - valorAproximado);
    
            System.out.printf("Valor real: %.3f%n", valorReal);
            System.out.printf("Valor aproximado: %.3f%n", valorAproximado);
            System.out.printf("Error numérico total: %.3f%n", error);
        }
    }

### Salida esperada del código:
    Valor real: 1.414  
    Valor aproximado: 1.414  
    Error numérico total: 0.000  
