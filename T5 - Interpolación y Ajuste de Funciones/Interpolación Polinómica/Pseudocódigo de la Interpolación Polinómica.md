# Tema 5: Interpolación Polinómica - Pseudocódigo
## Interpolación Polinómica
    Inicio
      Definir x como vector de reales [n]
      Definir y como vector de reales [n]
      Definir xp como real
      Definir yp como real
      Definir L como real
      Definir i, j como enteros
    
      x = [0, 1, 2, 3]
      y = [1, 2.718, 7.389, 20.085]
      xp = 1.5
      n = 4
      yp = 0
    
      Para i = 0 hasta n-1
        L = 1
        Para j = 0 hasta n-1
          Si j != i
            L = L * (xp - x[j]) / (x[i] - x[j])
          Fin Si
        Fin Para
        yp = yp + y[i] * L
      Fin Para
    
      Imprimir "Valor interpolado en x = ", xp, ": ", yp
    Fin
