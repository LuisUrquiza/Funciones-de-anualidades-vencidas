# Funciones de anualidades vencidas
# Cálculos de Anualidades Vencidas en R

## Valor Futuro
```R
valor_futuro = function(anualidad, tasa_interes, n_periodos) {
  return(anualidad * (((1 + tasa_interes) ^ n_periodos - 1) / tasa_interes))
}
Anualidad (conociendo valor futuro)


anualidad_por_valor_futuro = function(valor_futuro, tasa_interes, n_periodos) {
  return(valor_futuro * tasa_interes / (((1 + tasa_interes) ^ n_periodos - 1)))
}
Número de pagos o plazo (conociendo valor futuro)

numero_pagos_por_valor_futuro = function(valor_futuro, anualidad, tasa_interes) {
  return(log(valor_futuro * tasa_interes / anualidad + 1) / log(1 + tasa_interes))
}
Tasa del periodo (conociendo valor futuro)


Copiar
tasa_periodo_por_valor_futuro = function(valor_futuro, anualidad, n_periodos) {
  return((valor_futuro / anualidad) ^ (1 / n_periodos) - 1)
}
Valor Actual

valor_actual = function(anualidad, tasa_interes, n_periodos) {
  return(anualidad * (1 - (1 + tasa_interes) ^ -n_periodos) / tasa_interes)
}
Anualidad (conociendo valor actual)



anualidad_por_valor_actual = function(valor_actual, tasa_interes, n_periodios) {
  return(valor_actual * tasa_interes / (1 - (1 + tasa_interes) ^ -n_periodios))
}
Número de pagos o plazo (conociendo valor actual)

numero_pagos_por_valor_actual = function(valor_actual, anualidad, tasa_interes) {
  return(log(1 / (1 - valor_actual * tasa_interes / anualidad)) / log(1 + tasa_interes))
}
Tasa del periodo (conociendo valor actual)

