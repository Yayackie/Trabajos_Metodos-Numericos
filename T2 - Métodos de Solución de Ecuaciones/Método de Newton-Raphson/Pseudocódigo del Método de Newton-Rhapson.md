# Tema 2: Método de Newton-Raphson - Pseudocódigo
## Método de Newton-Raphson
    Inicio
      Función f(x)
        Retornar x^3 - x - 2
      Fin Función
    
      Función fPrima(x)
        Retornar 3 * x^2 - 1
      Fin Función
    
      Definir x como real
      Definir tolerancia como real
      Definir maxIteraciones como entero
      Definir iteracion como entero
      Definir fx como real
    
      x = 1.5
      tolerancia = 0.001
      maxIteraciones = 100
      iteracion = 0
    
      Mientras iteracion < maxIteraciones
        fx = f(x)
        Imprimir "Iteración ", iteracion, ": x = ", x, ", f(x) = ", fx
    
        Si abs(fx) < tolerancia
          Imprimir "Raíz encontrada: ", x
          Retornar
        Fin Si
    
        x = x - fx / fPrima(x)
        iteracion = iteracion + 1
      Fin Mientras
    
      Imprimir "Máximo de iteraciones alcanzado"
    Fin
