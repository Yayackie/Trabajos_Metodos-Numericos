# Tema 1: Error de Redondeo - Ejemplo en Java con salida esperada
## Error de Redondeo
        public class ErrorRedondeo {
        public static void main(String[] args) {
            double resultado = (1.0 / 3.0) * 3.0;
            double esperado = 1.0;
    
            System.out.println("Resultado calculado: " + resultado);
            System.out.println("Resultado esperado: " + esperado);
            System.out.println("Error de redondeo: " + Math.abs(esperado - resultado));
        }
    }

### Salida esperada del código:
    Resultado calculado: 0.9999999999999999  
    Resultado esperado: 1.0  
    Error de redondeo: 0.000  
