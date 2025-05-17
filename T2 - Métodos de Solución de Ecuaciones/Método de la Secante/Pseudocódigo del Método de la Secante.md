# Tema 2: Método de la Secante - Pseudocódigo
## Método de la Secante
    Inicio
      Función f(x)
        Retornar x^3 - x - 2
      Fin Función
    
      Definir x0 como real
      Definir x1 como real
      Definir tolerancia como real
      Definir maxIteraciones como entero
      Definir iteracion como entero
      Definir x2 como real
      Definir fx0 como real
      Definir fx1 como real
    
      x0 = 1.0
      x1 = 2.0
      tolerancia = 0.001
      maxIteraciones = 100
      iteracion = 0
    
      Mientras iteracion < maxIteraciones
        fx0 = f(x0)
        fx1 = f(x1)
        x2 = x1 - (fx1 * (x1 - x0)) / (fx1 - fx0)
        Imprimir "Iteración ", iteracion, ": x = ", x2, ", f(x) = ", f(x2)
    
        Si abs(f(x2)) < tolerancia
          Imprimir "Raíz encontrada: ", x2
          Retornar
        Fin Si
    
        x0 = x1
        x1 = x2
        iteracion = iteracion + 1
      Fin Mientras
    
      Imprimir "Máximo de iteraciones alcanzado"
    Fin
