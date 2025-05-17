# Tema 3: Método de Gauss-Seidel - Pseudocódigo
## Método de Gauss-Seidel
```
Inicio
  Definir n como entero
  Definir A como matriz de reales [n][n]
  Definir b como vector de reales [n]
  Definir x como vector de reales [n]
  Definir xNuevo como vector de reales [n]
  Definir tolerancia como real
  Definir maxIteraciones como entero
  Definir iteracion como entero
  Definir i, j como enteros
  Definir error como real

  n = 3
  A = [[3, 2, -1], [2, -2, 4], [-1, 0.5, -1]]
  b = [1, -2, 0]
  x = [0, 0, 0]
  tolerancia = 0.001
  maxIteraciones = 100
  iteracion = 0

  Mientras iteracion < maxIteraciones
    error = 0
    Para i = 0 hasta n-1
      Definir suma como real
      suma = 0
      Para j = 0 hasta n-1
        Si j != i
          suma = suma + A[i][j] * x[j]
        Fin Si
      Fin Para
      xNuevo[i] = (b[i] - suma) / A[i][i]
      error = max(error, abs(xNuevo[i] - x[i]))
      x[i] = xNuevo[i]
    Fin Para

    Imprimir "Iteración ", iteracion, ":"
    Para i = 0 hasta n-1
      Imprimir "x", i, " = ", x[i]
    Fin Para

    Si error < tolerancia
      Imprimir "Solución encontrada"
      Retornar
    Fin Si

    iteracion = iteracion + 1
  Fin Mientras

  Imprimir "Máximo de iteraciones alcanzado"
Fin
```
