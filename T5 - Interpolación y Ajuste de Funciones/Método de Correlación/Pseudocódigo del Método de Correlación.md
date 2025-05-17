# Tema 5: Método de Correlación - Pseudocódigo
## Método de Correlación
    Inicio
      Definir x como vector de reales [n]
      Definir y como vector de reales [n]
      Definir n como entero
      Definir sumX, sumY, sumXY, sumX2, sumY2 como reales
      Definir r como real
      Definir i como entero
    
      x = [0, 1, 2, 3]
      y = [1, 2.718, 7.389, 20.085]
      n = 4
      sumX = 0
      sumY = 0
      sumXY = 0
      sumX2 = 0
      sumY2 = 0
    
      Para i = 0 hasta n-1
        sumX = sumX + x[i]
        sumY = sumY + y[i]
        sumXY = sumXY + x[i] * y[i]
        sumX2 = sumX2 + x[i] * x[i]
        sumY2 = sumY2 + y[i] * y[i]
      Fin Para
    
      r = (n * sumXY - sumX * sumY) / sqrt((n * sumX2 - sumX * sumX) * (n * sumY2 - sumY * sumY))
    
      Imprimir "Coeficiente de correlación: ", r
    Fin
