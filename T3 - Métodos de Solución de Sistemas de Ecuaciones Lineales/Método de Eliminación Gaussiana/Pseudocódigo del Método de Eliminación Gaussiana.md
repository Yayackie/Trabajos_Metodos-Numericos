# Tema 3: Método de Eliminación Gaussiana - Pseudocódigo
## Método de Eliminación Gaussiana
    Inicio
      Definir n como entero
      Definir A como matriz de reales [n][n]
      Definir b como vector de reales [n]
      Definir x como vector de reales [n]
      Definir i, j, k como enteros
      Definir factor como real
    
      n = 3
      A = [[3, 2, -1], [2, -2, 4], [-1, 0.5, -1]]
      b = [1, -2, 0]
    
      // Eliminación hacia adelante
      Para k = 0 hasta n-2
        Si A[k][k] = 0
          Imprimir "Pivote nulo, no se puede resolver"
          Retornar
        Fin Si
        Para i = k+1 hasta n-1
          factor = A[i][k] / A[k][k]
          Para j = k hasta n-1
            A[i][j] = A[i][j] - factor * A[k][j]
          Fin Para
          b[i] = b[i] - factor * b[k]
        Fin Para
      Fin Para
    
      // Sustitución hacia atrás
      x[n-1] = b[n-1] / A[n-1][n-1]
      Para i = n-2 hasta 0 con paso -1
        Definir suma como real
        suma = 0
        Para j = i+1 hasta n-1
          suma = suma + A[i][j] * x[j]
        Fin Para
        x[i] = (b[i] - suma) / A[i][i]
      Fin Para
    
      Imprimir "Solución:"
      Para i = 0 hasta n-1
        Imprimir "x", i, " = ", x[i]
      Fin Para
    Fin
