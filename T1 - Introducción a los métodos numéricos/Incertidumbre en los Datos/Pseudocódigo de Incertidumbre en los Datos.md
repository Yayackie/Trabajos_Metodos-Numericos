# Tema 1: Incertidumbre en los Datos - Pseudocódigo

## Incertidumbre en los Datos
    Inicio
      Definir medicionOriginal como real
      Definir errorSensor como real
      Definir minimo como real
      Definir maximo como real
      medicionOriginal = 9.81
      errorSensor = 0.05
      minimo = medicionOriginal - errorSensor
      maximo = medicionOriginal + errorSensor
      Imprimir "Medición original: ", medicionOriginal
      Imprimir "Rango con incertidumbre: [", minimo, ", ", maximo, "]"
    Fin
