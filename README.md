# Dashboard de ventas: crecimiento real vs. inflación y devaluación

Proyecto de análisis de datos con Power BI sobre las ventas de mi propio emprendimiento (clases particulares, desde 2020). Partí de registros escritos a mano y construí un tablero que responde una pregunta concreta: **¿los ingresos crecieron de verdad, o solo acompañaron a la inflación?**

*English summary: Power BI dashboard built from my own small business sales records. I digitized handwritten data, cleaned it with Power Query (ETL), added USD exchange rate (JSON) and Argentina's CPI (CSV), and used DAX to compare nominal sales, USD sales and inflation-adjusted sales.*

## Vista previa

![Vista previa](capturas/dashboard-general.png)

## Qué hice

1. **Digitalización:** pasé a Excel los registros manuales de ventas e ingresos diarios.
2. **ETL con Power Query:** integré y depuré tres fuentes distintas: Excel (ventas), JSON (cotización del dólar) y CSV (IPC).
3. **Modelo de datos:** tablas de ventas, calendario, cotización del dólar e IPC, relacionadas por fecha.
4. **Medidas en DAX:** ventas totales, ticket promedio, margen de rentabilidad, crecimiento por período, ventas en USD y ventas ajustadas por IPC.
5. **Tablero interactivo:** ventas en pesos, en dólares y ajustadas por inflación, con filtros por año.

## Qué encontré

- **La demanda se concentra en fechas de examen.** Los picos de ventas coinciden con los períodos de exámenes, como julio y noviembre/diciembre.
- **Los ingresos crecieron también en términos reales.** Al ajustar por inflación, la curva sigue en ascenso sostenido. No es solo efecto de los precios.
- **En dólares la tendencia es similar:** los ingresos mensuales crecen a lo largo del período analizado.
- Los primeros meses muestran valores bajos porque el emprendimiento recién empezaba.

## Limitaciones

- **Faltan los registros de septiembre a diciembre de 2025** (el registro físico original se dañó). En el gráfico de línea ese tramo une agosto 2025 con enero 2026, así que **no refleja datos reales**. El tablero lo aclara con una nota.
- Los datos se cargan manualmente. No es un tablero en tiempo real.
- [Completar: qué serie o división del IPC usaste y cómo ajustaste las ventas.]

## Próximo paso

Reconstruir las ventas de ese período faltante a partir de los movimientos bancarios y comparar el resultado con los registros que sí se conservan.

## Archivos

| Archivo | Contenido |
|---|---|
| `dashboard_ventas.pbix` | Tablero de Power BI |
| `Datos_Mi_Negocio.xlsx` | Registro de ventas |
| `cotizacion_dolar.json` | Cotización del dólar |
| `serie_ipc_divisiones.csv` | Serie del IPC |
| `informe.pdf` | Informe del análisis |

Para abrirlo hace falta Power BI Desktop. Si cambiás de lugar los archivos de datos, hay que actualizar las rutas en Power Query.

## Herramientas

Power BI · Power Query · DAX · Excel · JSON · CSV


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
