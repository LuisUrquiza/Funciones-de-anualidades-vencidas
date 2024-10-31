# Funciones de anualidades vencidas
En este repositorio se encuentra un archivo Readme que recopila un conjunto de funciones para calcular anualidades vencidas así como las variables relacionadas con este tema
# Cálculos de Anualidades Vencidas

## Valor Futuro
```python
def valor_futuro(anualidad, tasa_interes, n_periodos):
    return anualidad * (((1 + tasa_interes) ** n_periodos - 1) / tasa_interes)
Anualidad (conociendo valor futuro)
python

def anualidad_por_valor_futuro(valor_futuro, tasa_interes, n_periodos):
    return valor_futuro * tasa_interes / (((1 + tasa_interes) ** n_periodos - 1))
Número de pagos o plazo (conociendo valor futuro)
python


import math

def numero_pagos_por_valor_futuro(valor_futuro, anualidad, tasa_interes):
    return math.log(valor_futuro * tasa_interes / anualidad + 1) / math.log(1 + tasa_interes)
Tasa del periodo (conociendo valor futuro)
python


def tasa_periodo_por_valor_futuro(valor_futuro, anualidad, n_periodos):
    return (valor_futuro / anualidad) ** (1 / n_periodos) - 1
Valor Actual
python


def valor_actual(anualidad, tasa_interes, n_periodos):
    return anualidad * (1 - (1 + tasa_interes) ** -n_periodos) / tasa_interes
Anualidad (conociendo valor actual)
python


def anualidad_por_valor_actual(valor_actual, tasa_interes, n_periodos):
    return valor_actual * tasa_interes / (1 - (1 + tasa_interes) ** -n_periodos)
Número de pagos o plazo (conociendo valor actual)
python


def numero_pagos_por_valor_actual(valor_actual, anualidad, tasa_interes):
    return math.log(1 / (1 - valor_actual * tasa_interes / anualidad)) / math.log(1 + tasa_interes)
Tasa del periodo (conociendo valor actual)
python


def tasa_periodo_por_valor_actual(valor_actual, anualidad, n_periodos):
    return (anualidad / valor_actual) ** (1 / n_periodos) - 1


