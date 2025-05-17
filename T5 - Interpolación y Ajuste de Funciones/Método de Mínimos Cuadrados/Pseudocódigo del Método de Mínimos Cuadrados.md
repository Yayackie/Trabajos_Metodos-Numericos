# Tema 5: Método de Mínimos Cuadrados - Pseudocódigo
## Método de Mínimos Cuadrados
    Inicio
      Definir x como vector de reales [n]
      Definir y como vector de reales [n]
      Definir n como entero
      Definir sumX, sumY, sumXY, sumX2 como reales
      Definir m, b como reales
      Definir i como entero
    
      x = [0, 1, 2, 3]
      y = [1, 2.718, 7.389, 20.085]
      n = 4
      sumX = 0
      sumY = 0
      sumXY = 0
      sumX2 = 0
    
      Para i = 0 hasta n-1
        sumX = sumX + x[i]
        sumY = sumY + y[i]
        sumXY = sumXY + x[i] * y[i]
        sumX2 = sumX2 + x[i] * x[i]
      Fin Para
    
      m = (n * sumXY - sumX * sumY) / (n * sumX2 - sumX * sumX)
      b = (sumY - m * sumX) / n
    
      Imprimir "Ecuación de la recta: y = ", m, "x + ", b
    Fin
