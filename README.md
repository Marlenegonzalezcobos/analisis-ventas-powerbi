# 📊 Dashboard de análisis de ventas e inteligencia de negocios (Power BI)

Dashboard interactivo en **Power BI** que transforma los registros de ventas e ingresos diarios de mi emprendimiento (clases particulares de Química Biológica) en indicadores claros para tomar decisiones, y que además compara la evolución de los ingresos con la **inflación (IPC)** y la **cotización del dólar**.

![Vista general del dashboard](capturas/dashboard-general.png)

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

> Completar con 3 o 4 conclusiones concretas, por ejemplo:
> - [Qué días y horarios tienen más demanda]
> - [Qué servicio o producto es el más rentable]
> - [Si los ingresos acompañaron o no a la inflación en el período analizado]

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
