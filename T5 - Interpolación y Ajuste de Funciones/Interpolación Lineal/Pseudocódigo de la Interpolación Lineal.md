# Tema 5: Interpolación Lineal - Pseudocódigo
## Interpolación Lineal
    Inicio
      Definir x como vector de reales [n]
      Definir y como vector de reales [n]
      Definir xp como real
      Definir yp como real
      Definir i como entero
    
      x = [0, 1, 2, 3]
      y = [1, 2.718, 7.389, 20.085]
      xp = 1.5
      n = 4
    
      Para i = 0 hasta n-2
        Si x[i] <= xp Y xp <= x[i+1]
          yp = y[i] + (y[i+1] - y[i]) * (xp - x[i]) / (x[i+1] - x[i])
          Imprimir "Valor interpolado en x = ", xp, ": ", yp
          Retornar
        Fin Si
      Fin Para
    
      Imprimir "Punto fuera del rango de interpolación"
    Fin
