# Tema 1: Incertidumbre en los Datos - Ejemplo en Java con salida esperada

## Incertidumbre en los Datos
    public class IncertidumbreDatos {
        public static void main(String[] args) {
            double valorMedido = 100.0;
            double margenError = 2.5;
    
            double minimo = valorMedido - margenError;
            double maximo = valorMedido + margenError;
    
            System.out.printf("Valor medido: %.3f%n", valorMedido);
            System.out.printf("Rango estimado: [%.3f, %.3f]%n", minimo, maximo);
            System.out.printf("Incertidumbre en los datos: ±%.3f%n", margenError);
        }
    }

### Salida esperada del código:
    Valor medido: 100.000  
    Rango estimado: [97.500, 102.500]  
    Incertidumbre en los datos: ±2.500  
