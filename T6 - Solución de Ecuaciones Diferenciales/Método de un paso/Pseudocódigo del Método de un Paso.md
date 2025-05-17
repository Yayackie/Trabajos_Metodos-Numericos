# Tema 6: Método de un paso - Pseudocódigo
## Método de un paso
    Inicio
      Función f(x, y)
        Retornar -2 * x * y
      Fin Función
    
      Definir a como real
      Definir b como real
      Definir h como real
      Definir n como entero
      Definir x como vector de reales [n+1]
      Definir y como vector de reales [n+1]
      Definir i como entero
      Definir k1, k2 como reales
    
      a = 0.0
      b = 1.0
      h = 0.2
      n = 5
      y[0] = 1.0
    
      Para i = 0 hasta n
        x[i] = a + i * h
      Fin Para
    
      Para i = 0 hasta n-1
        k1 = f(x[i], y[i])
        k2 = f(x[i] + h, y[i] + h * k1)
        y[i+1] = y[i] + (h / 2) * (k1 + k2)
      Fin Para
    
      Para i = 0 hasta n
        Imprimir "x = ", x[i], ", y = ", y[i]
      Fin Para
    Fin
