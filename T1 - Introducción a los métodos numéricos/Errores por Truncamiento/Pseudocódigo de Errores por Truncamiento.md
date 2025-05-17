# Tema 1: Error de Truncamiento - Pseudocódigo
## Error de Truncamiento
    Inicio
      Función funciónReal(x)
        Retornar exp(x)
      Fin Función
    
      Función aproximacionTaylor(x, n)
        Definir suma como real
        Definir i como entero
        suma = 0
        Para i = 0 hasta n
          suma = suma + (x^i) / factorial(i)
        Fin Para
        Retornar suma
      Fin Función
    
      Definir x como real
      Definir n como entero
      Definir real como real
      Definir aproximado como real
      x = 1.0
      n = 3
      real = funciónReal(x)
      aproximado = aproximacionTaylor(x, n)
      Imprimir "Valor real: ", real
      Imprimir "Aproximación: ", aproximado
      Imprimir "Error de truncamiento: ", abs(real - aproximado)
    Fin
