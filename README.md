# Dashboard de análisis de ventas e inteligencia de negocios

Tablero interactivo en Power BI construido a partir de los registros de ventas de mi propio emprendimiento (clases particulares). Busca responder tres cosas: cómo evolucionan los ingresos en el tiempo, si acompañan a la inflación y en qué momentos se concentra la demanda.

**Herramientas:** Power BI · Power Query · DAX · Excel · JSON · CSV

## Preguntas que responde el análisis

- ¿Cuáles son los productos de mayor rotación y los días de mayor demanda?
- ¿Los ingresos crecieron en términos reales o solo en pesos corrientes?
- ¿Cómo se ven los ingresos expresados en dólares?
- ¿En qué épocas del año se concentra la demanda?

## Datos

| Fuente | Archivo | Contenido |
|---|---|---|
| Ventas e ingresos diarios | `Datos_Mi_Negocio.xlsx` | Registros escritos a mano, digitalizados en Excel |
| Cotización del dólar blue | `blue.json` | Serie de cotización usada para expresar los ingresos en USD |
| Inflación | `serie_ipc_divisiones.csv` | Serie de IPC por divisiones, usada para ajustar los ingresos por inflación |

**Período analizado:** septiembre de 2024 a septiembre de 2026 (el ajuste por inflación llega hasta agosto de 2026).

**Dato faltante:** no hay registros de septiembre a diciembre de 2025, porque los registros físicos originales se dañaron. Ese tramo aparece sin datos en el análisis.

## Metodología

1. **ETL con Power Query:** integración y limpieza de fuentes heterogéneas (Excel, JSON y CSV), con transformaciones para unificar formatos y fechas.
2. **Modelo de datos y medidas en DAX:**
   - Ventas totales, ticket promedio, margen de rentabilidad y crecimiento por período.
   - Ventas reales ajustadas por inflación (IPC), con base en septiembre de 2024.
   - Ventas en dólares (cotización blue).
3. **Visualización:** tablero interactivo con una vista de ingresos mensuales en USD y otra de ventas nominales frente a ventas reales ("¿Crecimiento real o inflación?").

## Hallazgos

- Ajustados por inflación, los ingresos crecieron de forma sostenida: el aumento no se explica solo por la suba de precios general.
- La demanda se concentra en épocas de examen, con picos que se repiten en julio de un año a otro.
- Expresados en dólares, los ingresos también muestran una tendencia creciente, con los valores más altos durante 2026.
- Hubo tramos sin crecimiento real, como enero a abril de 2026, posiblemente asociados a la estacionalidad.

## Limitaciones

- La falta de datos de septiembre a diciembre de 2025 deja afuera meses de alta demanda. Por eso no conviene comparar años calendario completos; es más justo comparar el mismo mes entre años.
- El análisis mide ingresos: no distingue si el crecimiento vino de más clases, de cambios de precio o de ambos.

## Próximos pasos

Segundo proyecto: reconstruir los registros faltantes cruzando los movimientos bancarios con los datos existentes, para completar el análisis.

## Cómo explorar el proyecto

- Abrir `archivopowebi.pbix` con Power BI Desktop.
- O ver el resumen del tablero en `informe.pdf`.

## Autora

**Marlene Gonzalez Cobos** · Estudiante de Tecnicatura en Análisis de Sistemas Informáticos
[LinkedIn](https://linkedin.com/in/marlene-g-cobos/) · [GitHub](https://github.com/Marlenegonzalezcobos)
