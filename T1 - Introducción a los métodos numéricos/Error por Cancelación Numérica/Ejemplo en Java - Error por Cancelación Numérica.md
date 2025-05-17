# Tema 1: Error por Cancelación Numérica - Ejemplo en Java con salida esperada

## Error por Cancelación Numérica
    public class CancelacionNumerica {
        public static void main(String[] args) {
            double a = 1.0000001;
            double b = 1.0000000;
    
            double resultado = a - b;
    
            System.out.printf("Resultado esperado: %.7f%n", 0.0000001);
            System.out.printf("Resultado real: %.7f%n", resultado);
            System.out.println("Este tipo de resta puede causar pérdida de precisión.");
        }
    }

### Salida esperada del código:
    Resultado esperado: 0.0000001  
    Resultado real: 0.0000001  
    Este tipo de resta puede causar pérdida de precisión.
