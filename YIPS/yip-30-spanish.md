---
YIP: 30
Título: Calendario de inflación de YFI
Estado: Rechazada
Autor: Substreight (@substreight), DeltaTiger (@deltatigernz), Hannes Graah (@Graadient), Daryl Lau (@Daryllautk), yfi_whale
Discusiones: https://gov.yearn.finance/t/yip-30-yfi-inflation-schedule/1439
Fecha de creación: 2020-07-28
---

## Explicación corta

Implementar un calendario de inflación de 20,000 YFI a lo largo de los próximos 8 años, de los cuales 12,802 serán distribuídos los 3 primeros años, acabando con un 1% de inflación.

## Resumen

* Actualizar el contrato de creación de YFI para ajustarse al nuevo calendario de inflación.

## Motivación

Crear un calendario de inflación después de la aprobación de la YIP-0.

**A FAVOR**: Implementar un calendario de inflación de 20,000 YFI a lo largo de 8 años, con 12,802 distribuídos en los 3 primeros años, acabando con un 1% de inflación.

**EN CONTRA**: No se hace ningún cambio.

## Especificación

### Visión general

1. Ajustar el calendario de inflación para seguir [[este modelo](https://docs.google.com/spreadsheets/d/1yomUGpAWR8svL9RXD-_vL2ArgQPGj1x2XPNKDEuZR9Q/edit?usp=sharing)].
  - Inflación anual inicial: 22.384%
  - Multiplicador reductor semanal de emisiones: 0.9937
  - Semana en la que empieza la inflación final: semana 416
  - Porcentaje fijo de inflación final (cola de emisión): 1%
2. Este modelo permanecerá inalterado hasta que acabe la emisión o se haga un ajuste.

### Razonamiento fundamental

* El rendimiento de los proveedores de liquidez se mantiene a niveles razonadamente competitivos en varios escenarios del precio de YFI y el valor total depositado en el protocolo (ver la hoja del modelo).
* Menor inflación inicial (22%) para mantener las recompensas a largo plazo dentro de unos límites razonables.
* 8 años de emisión programada para incentivar el desarrollo a largo plazo.

Referencia: [synthetix/contracts/SupplySchedule.sol](https://github.com/Synthetixio/synthetix/blob/master/contracts/SupplySchedule.sol)

## Metadatos

| Nombre               | Valor                                      |
|---------------------|--------------------------------------------|
| Propuesta por         | 0x2D407dDb06311396fE14D4b49da5F0471447d45C |
| Votos totales a favor     | 3380.7051 (38.73%)                         |
| Votos totales en contra | 5346.6313 (61.26%)                         |
| Quorum              | 82.39% ✔                                   |
| Bloque inicial         | 10560113                                   |
| Bloque final           | 10577393                                   |

Fuente: [yieldfarming.info YFI Governance Information](https://yieldfarming.info/yearn/vote/)

## Derechos de autor
Derechos de autor y derechos relacionados con renuncia a través de [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
