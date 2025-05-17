# Tema 4: Método de Simpson 3/8 - Pseudocódigo
## Método de Simpson 3/8
    Inicio
      Función f(x)
        Retornar exp(x)
      Fin Función
    
      Definir a como real
      Definir b como real
      Definir n como entero
      Definir h como real
      Definir suma como real
      Definir x como real
      Definir i como entero
      Definir integral como real
    
      a = 0.0
      b = 1.0
      n = 3
    
      Si n mod 3 != 0
        Imprimir "El número de subintervalos debe ser múltiplo de 3"
        Retornar
      Fin Si
    
      h = (b - a) / n
      suma = f(a) + f(b)
    
      Para i = 1 hasta n-1
        x = a + i * h
        Si i mod 3 = 0
          suma = suma + 2 * f(x)
        Sino
          suma = suma + 3 * f(x)
        Fin Si
      Fin Para
    
      integral = (3 * h / 8) * suma
      Imprimir "Integral aproximada: ", integral
    Fin
