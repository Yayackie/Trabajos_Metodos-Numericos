# Tema 4: Método del Trapecio - Pseudocódigo
## Método del Trapecio
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
      n = 4
    
      h = (b - a) / n
      suma = f(a) + f(b)
    
      Para i = 1 hasta n-1
        x = a + i * h
        suma = suma + 2 * f(x)
      Fin Para
    
      integral = (h / 2) * suma
      Imprimir "Integral aproximada: ", integral
    Fin
