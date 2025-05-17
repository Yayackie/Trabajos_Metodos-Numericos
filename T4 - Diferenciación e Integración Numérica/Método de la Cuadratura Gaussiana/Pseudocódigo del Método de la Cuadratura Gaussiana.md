# Tema 4: Método de la Cuadratura Gaussiana - Pseudocódigo
## Método de la Cuadratura Gaussiana
    Inicio
      Función f(x)
        Retornar exp(x)
      Fin Función
    
      Definir a como real
      Definir b como real
      Definir n como entero
      Definir puntos como vector de reales [n]
      Definir pesos como vector de reales [n]
      Definir suma como real
      Definir t como real
      Definir x como real
      Definir i como entero
      Definir integral como real
    
      a = 0.0
      b = 1.0
      n = 3
      puntos = [-0.774596669, 0.0, 0.774596669]
      pesos = [0.555555556, 0.888888889, 0.555555556]
    
      suma = 0
      Para i = 0 hasta n-1
        t = puntos[i]
        x = ((b - a) * t + (b + a)) / 2
        suma = suma + pesos[i] * f(x)
      Fin Para
    
      integral = ((b - a) / 2) * suma
      Imprimir "Integral aproximada: ", integral
    Fin
