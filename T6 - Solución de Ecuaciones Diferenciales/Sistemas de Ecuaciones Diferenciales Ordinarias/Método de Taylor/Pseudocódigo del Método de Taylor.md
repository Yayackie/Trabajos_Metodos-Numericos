# Tema 6: Método de Taylor - Pseudocódigo
## Método de Taylor
    Inicio
      Función f(x, y)
        Retornar -2 * x * y
      Fin Función
    
      Función fPrima(x, y)
        Retornar -2 * y - 2 * x * (-2 * x * y)
      Fin Función
    
      Definir a como real
      Definir b como real
      Definir h como real
      Definir n como entero
      Definir x como vector de reales [n+1]
      Definir y como vector de reales [n+1]
      Definir i como entero
    
      a = 0.0
      b = 1.0
      h = 0.2
      n = 5
      y[0] = 1.0
    
      Para i = 0 hasta n
        x[i] = a + i * h
      Fin Para
    
      Para i = 0 hasta n-1
        y[i+1] = y[i] + h * f(x[i], y[i]) + (h^2 / 2) * fPrima(x[i], y[i])
      Fin Para
    
      Para i = 0 hasta n
        Imprimir "x = ", x[i], ", y = ", y[i]
      Fin Para
    Fin
