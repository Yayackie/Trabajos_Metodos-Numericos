# Tema 1: Errores de Formulación - Ejemplo en Java con salida esperada

## Errores de Formulación
    public class ErrorFormulacion {
        public static void main(String[] args) {
            double g = 9.81;
            double tiempo = 3.0;
    
            double distanciaIdeal = 0.5 * g * Math.pow(tiempo, 2);
    
            System.out.printf("Distancia (modelo ideal): %.3f metros%n", distanciaIdeal);
            System.out.println("Nota: No se considera resistencia del aire.");
        }
    }

### Salida esperada del código:
    Distancia (modelo ideal): 44.145 metros  
    Nota: No se considera resistencia del aire.
