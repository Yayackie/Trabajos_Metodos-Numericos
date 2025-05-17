# Tema 1: Errores por Equivocación - Ejemplo en Java con salida esperada

## Errores por Equivocación
    public class ErrorEquivocacion {
        public static void main(String[] args) {
            double radio = 5.0;
    
            double areaIncorrecta = Math.PI * radio * 2;
            double areaCorrecta = Math.PI * Math.pow(radio, 2);
    
            System.out.printf("Área incorrecta: %.3f%n", areaIncorrecta);
            System.out.printf("Área correcta: %.3f%n", areaCorrecta);
            System.out.printf("Diferencia: %.3f%n", Math.abs(areaCorrecta - areaIncorrecta));
        }
    }

### Salida esperada del código:
    Área incorrecta: 31.416  
    Área correcta: 78.540  
    Diferencia: 47.124  
