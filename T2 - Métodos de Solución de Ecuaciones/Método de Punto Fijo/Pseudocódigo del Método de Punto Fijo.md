# Tema 2: Método de Punto Fijo - Pseudocódigo
## Método de Punto Fijo
    Inicio
      Función f(x)
        Retornar x^3 - x - 2
      Fin Función
    
      Función g(x)
        Retornar (x + 2)^(1/3)
      Fin Función
    
      Definir x como real
      Definir tolerancia como real
      Definir maxIteraciones como entero
      Definir iteracion como entero
      Definir xNuevo como real
    
      x = 1.5
      tolerancia = 0.001
      maxIteraciones = 100
      iteracion = 0
    
      Mientras iteracion < maxIteraciones
        xNuevo = g(x)
        Imprimir "Iteración ", iteracion, ": x = ", xNuevo, ", f(x) = ", f(xNuevo)
    
        Si abs(xNuevo - x) < tolerancia
          Imprimir "Raíz encontrada: ", xNuevo
          Retornar
        Fin Si
    
        x = xNuevo
        iteracion = iteracion + 1
      Fin Mientras
    
      Imprimir "Máximo de iteraciones alcanzado"
    Fin
