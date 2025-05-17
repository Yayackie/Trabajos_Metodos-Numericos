# Tema 2: Método de Bisección - Pseudocódigo
## Método de Bisección
    Inicio
      Función f(x)
        Retornar x^3 - x - 2
      Fin Función
    
      Definir a como real
      Definir b como real
      Definir tolerancia como real
      Definir maxIteraciones como entero
      Definir iteracion como entero
      Definir p como real
      Definir fa como real
      Definir fb como real
      Definir fp como real
    
      a = 1.0
      b = 2.0
      tolerancia = 0.001
      maxIteraciones = 100
      iteracion = 0
    
      fa = f(a)
      fb = f(b)
    
      Si fa * fb >= 0
        Imprimir "El intervalo no contiene una raíz"
        Retornar
      Fin Si
    
      Mientras iteracion < maxIteraciones
        p = (a + b) / 2
        fp = f(p)
        Imprimir "Iteración ", iteracion, ": x = ", p, ", f(x) = ", fp
    
        Si abs(fp) < tolerancia O abs(b - a) < tolerancia
          Imprimir "Raíz encontrada: ", p
          Retornar
        Fin Si
    
        Si fa * fp < 0
          b = p
          fb = fp
        Sino
          a = p
          fa = fp
        Fin Si
    
        iteracion = iteracion + 1
      Fin Mientras
    
      Imprimir "Máximo de iteraciones alcanzado"
    Fin
