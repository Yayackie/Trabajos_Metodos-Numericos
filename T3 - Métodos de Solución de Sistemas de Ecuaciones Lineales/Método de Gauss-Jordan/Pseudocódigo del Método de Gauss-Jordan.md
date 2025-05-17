# Tema 3: Método de Gauss-Jordan - Pseudocódigo
## Método de Gauss-Jordan
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
    
      // Eliminación hacia adelante y hacia atrás
      Para k = 0 hasta n-1
        Si A[k][k] = 0
          Imprimir "Pivote nulo, no se puede resolver"
          Retornar
        Fin Si
        // Normalizar fila k
        factor = A[k][k]
        Para j = 0 hasta n-1
          A[k][j] = A[k][j] / factor
        Fin Para
        b[k] = b[k] / factor
    
        // Eliminar columna k en otras filas
        Para i = 0 hasta n-1
          Si i != k
            factor = A[i][k]
            Para j = 0 hasta n-1
              A[i][j] = A[i][j] - factor * A[k][j]
            Fin Para
            b[i] = b[i] - factor * b[k]
          Fin Si
        Fin Para
      Fin Para
    
      // Solución
      Para i = 0 hasta n-1
        x[i] = b[i]
      Fin Para
    
      Imprimir "Solución:"
      Para i = 0 hasta n-1
        Imprimir "x", i, " = ", x[i]
      Fin Para
    Fin
