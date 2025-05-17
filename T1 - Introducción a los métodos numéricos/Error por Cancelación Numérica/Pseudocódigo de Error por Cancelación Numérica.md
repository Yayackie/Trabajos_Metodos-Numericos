# Tema 1: Error por Cancelación Numérica - Pseudocódigo
## Error por Cancelación Numérica
    Inicio
      Definir a como real
      Definir b como real
      Definir resultado como real
      a = 1.0000001
      b = 1.0000000
      resultado = a - b
      Imprimir "Resultado esperado: 0.0000001"
      Imprimir "Resultado real: ", resultado
      Imprimir "Error por cancelación: ", abs(0.0000001 - resultado)
    Fin
