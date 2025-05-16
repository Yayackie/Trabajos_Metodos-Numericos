# Tema 1: Tipos de Errores Numéricos - Ejemplos en Java

## Introducción

En este apartado encontrarás ejemplos reales implementados en Java para observar en acción los distintos tipos de errores numéricos. Estos ejemplos te permitirán entender mejor cómo surgen y cómo afectan los cálculos numéricos en la práctica. Cada código va acompañado de su **salida esperada** con los resultados redondeados a tres cifras decimales.

## 1. Error de Redondeo
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


## 2. Error de Truncamiento
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

## 3. Error Numérico Total
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

## 4. Errores por Equivocación
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


## 5. Errores de Formulación
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

## 6. Incertidumbre en los Datos
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

## 7. Error por Cancelación Numérica
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
