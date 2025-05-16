# Tema 2: Tipos de Errores Numéricos - Pseudocódigo en Java

## Introducción

En esta sección encontrarás una representación en pseudocódigo (con estilo Java) de cómo simular o identificar cada tipo de error numérico descrito en la teoría. Estos fragmentos no son soluciones completas, sino ejemplos prácticos que ilustran cómo aparecen y se pueden analizar estos errores en implementaciones numéricas.

---

## 1. Error de Redondeo
    public class ErrorRedondeo {
    public static void main(String[] args) {
        double a = 1.0 / 3.0;
        double b = a * 3.0;

        System.out.println("Resultado teórico: 1.0");
        System.out.println("Resultado real: " + b);
        System.out.println("Error de redondeo: " + (1.0 - b));
    } 
    }

## 2. Error de Truncamiento

    public class ErrorTruncamiento {
    public static double funcionReal(double x) {
        return Math.exp(x); // valor real usando la función nativa
    }

    public static void main(String[] args) {
        double x = 1.0;
        int n = 3;
        double real = funcionReal(x);
        double aproximado = aproximacionTaylor(x, n);

        System.out.println("Valor real: " + real);
        System.out.println("Aproximación: " + aproximado);
        System.out.println("Error de truncamiento: " + Math.abs(real - aproximado));
    }
    }
## 3. Error Numérico Total
    public class ErrorTotal {

    public static void main(String[] args) {
    
        double real = Math.sqrt(2); // valor exacto
        double aproximado = 1.4142; // valor aproximado
        double errorTotal = Math.abs(real - aproximado);
        System.out.println("Valor real: " + real);
        System.out.println("Valor aproximado: " + aproximado);
        System.out.println("Error numérico total: " + errorTotal);
    }
    }
## 4. Errores por Equivocación
    public class ErrorEquivocacion {
    public static void main(String[] args) {
        // Ejemplo de error humano: cálculo mal implementado
        double areaCorrecta = Math.PI * Math.pow(5, 2);
        double areaConError = 3.14 * 5 * 2; // Error: fórmula incorrecta

        System.out.println("Área correcta: " + areaCorrecta);
        System.out.println("Área mal calculada (por equivocación): " + areaConError);
    }
    }
## 5. Errores de Formulación
    public class ErrorFormulacion {
    public static void main(String[] args) {
        // Modelo simplificado: caída libre sin resistencia del aire
        double g = 9.81; // gravedad
        double t = 3.0; // tiempo
        double distanciaIdeal = 0.5 * g * Math.pow(t, 2);

        // Supuesto incorrecto: desprecia resistencia del aire
        System.out.println("Distancia sin resistencia del aire (modelo simplificado): " + distanciaIdeal);
        System.out.println("Nota: Este resultado no considera factores reales del entorno.");
    }
    }

## 6. Incertidumbre en los Datos
    public class IncertidumbreDatos {
    public static void main(String[] args) {
        double medicionOriginal = 9.81;
        double errorSensor = 0.05; // ±0.05 m/s²

        double minimo = medicionOriginal - errorSensor;
        double maximo = medicionOriginal + errorSensor;

        System.out.println("Medición original: " + medicionOriginal);
        System.out.println("Rango con incertidumbre: [" + minimo + ", " + maximo + "]");
    }
    }

## 7. Error por Cancelación Numérica
    public class CancelacionNumerica {
    public static void main(String[] args) {
        double a = 1.0000001;
        double b = 1.0000000;
        double resultado = a - b;

        System.out.println("Resultado esperado: 0.0000001");
        System.out.println("Resultado real (posible cancelación): " + resultado);
    }
    }

Estos ejemplos muestran cómo pueden aparecer los errores numéricos en algoritmos sencillos, y permiten analizar su impacto en los resultados. En implementaciones reales, es importante identificar y minimizar estos errores para obtener soluciones más confiables, especialmente en aplicaciones científicas, de ingeniería y sistemas críticos.



