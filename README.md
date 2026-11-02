# 📊 Dashboard de análisis de ventas e inteligencia de negocios (Power BI)

Dashboard interactivo en **Power BI** que transforma los registros de ventas e ingresos diarios de mi emprendimiento (clases particulares de Química Biológica) en indicadores claros para tomar decisiones, y que además compara la evolución de los ingresos con la **inflación (IPC)** y la **cotización del dólar**.

[Vista general del dashboard](capturas/dashboard-general.png)

### Ingresos mensuales en dólares
![Ingresos mensuales en USD](capturas/ingresos-usd.png)

### ¿Crecimiento real o inflación?
![Ventas nominales vs. ventas reales ajustadas](capturas/crecimiento-vs-inflacion.png)

## 🎯 Objetivo

Pasar de anotaciones hechas a mano a un sistema de análisis que responda preguntas como:

- ¿Cuánto vendo por período y cómo evoluciona el crecimiento?
- ¿Cuál es el ticket promedio y el margen de rentabilidad?
- ¿Qué días y horarios concentran más demanda?
- ¿Mis ingresos le ganan a la inflación o la acompañan?

## 🗂️ Fuentes de datos

| Archivo | Formato | Contenido |
|---|---|---|
| `datos/Datos_Mi_Negocio.xlsx` | Excel | Registro de ventas e ingresos diarios (digitalizado desde papel) |
| `datos/blue.json` | JSON | Cotización del dólar blue |
| `datos/serie_ipc_divisiones.csv` | CSV | Serie del IPC por divisiones |

## ⚙️ Proceso

1. **Digitalización:** pasé los registros manuales a Excel.
2. **ETL con Power Query:** extracción, limpieza y transformación de las tres fuentes (Excel, JSON y CSV) para unificar formatos y fechas.
3. **Modelo de datos:** relaciones entre ventas, calendario, cotización e IPC.
4. **Medidas en DAX:** cálculo de KPIs.
5. **Visualización:** tablero interactivo con filtros por período.

## 📈 KPIs principales

- Ventas totales
- Ticket promedio por transacción
- Margen de rentabilidad
- Crecimiento de ventas por período
- Ingresos reales vs. inflación

## 🔍 Principales hallazgos

- Comparando enero–agosto de 2026 con el mismo período de 2025, las ventas
  nominales en pesos crecieron un 88,9%, mientras que las ventas reales
  (ajustadas por IPC, a pesos de septiembre de 2024) crecieron un 42,2%:
  los ingresos superaron a la inflación.
- Julio de 2026 fue el mes de mayores ingresos de la serie (en dólares).
- [Un tercer hallazgo: por ejemplo, qué meses del año suelen ser más bajos]

⚠️ Septiembre–diciembre de 2025 no tienen datos (registros físicos
dañados), por lo que se excluyeron de las comparaciones.

⚠️ Septiembre–diciembre de 2025 no tienen datos (registros físicos dañados),
por lo que se excluyen de las comparaciones.

## ⚠️ Limitaciones

- Parte de los registros físicos de [período] se dañaron y no pudieron
  digitalizarse, por lo que los datos de esos meses están incompletos.
- Próximo paso: reconstruir esos períodos a partir de los movimientos
  bancarios (ver proyecto 2, en desarrollo).

## 🛠️ Tecnologías

Power BI · Power Query · DAX · Excel · JSON · CSV

## 📁 Estructura del repositorio

```
├── README.md
├── dashboard/
│   ├── dashboard-ventas.pbix
├── datos/
│   ├── Datos_Mi_Negocio.xlsx
│   ├── blue.json
│   └── serie_ipc_divisiones.csv
└── capturas/
    └── dashboard-general.png
```

## ▶️ Cómo abrirlo

1. Descargá el repositorio (**Code → Download ZIP**).
2. Abrí `dashboard/dashboard-ventas.pbix` con **Power BI Desktop** (gratuito).
3. Si Power BI pide actualizar las rutas, apuntá a la carpeta `datos/`.

## 👩‍💻 Autora

**Marlene González Cobos**, estudiante de Análisis de Sistemas Informáticos.
[LinkedIn](https://linkedin.com/in/marlene-g-cobos/) · [GitHub](https://github.com/Marlenegonzalezcobos)
