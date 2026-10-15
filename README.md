# 📊 Análisis de Ventas: Crecimiento Real vs. Inflación y Devaluación

## 🎯 Pregunta de Investigación
¿Las ganancias del emprendimiento están creciendo realmente o solo acompañan la inflación y las devaluaciones del mercado?

## 👥 Integrantes y Roles
- **Marlene Gonzalez Cobos**: Extracción, Transformación y Carga (ETL) en Power Query.
- **Guadalupe Loyola**: Arquitectura del Modelo de Datos (Star Schema) y Medidas DAX.
- **Santiago Alfredo Villagra**: Diseño del Tablero (UI/UX) y Presentación Ejecutiva.

## 🛠️ Fuentes de Datos
1. **Ventas del emprendimiento (`Datos_Mi_Negocio.xlsx`)**: Granularidad transaccional (diaria).
2. **Índices de precios al consumidor (`serie_ipc_divisiones.csv`)**: IPC Regional/Nacional (Granularidad mensual).
3. **Cotización Dólar Blue (`blue.json`)**: Histórico de cotización diaria.

## 📐 Modelo de Datos y Medidas DAX
- **Modelo Star Schema** con dimensión `Calendario` centralizada para resolver discrepancias de granularidad.
- **Métricas principales**:
  - `Ventas_Nominales_ARS`: Facturación bruta acumulada.
  - `Ventas_Reales_Ajustadas`: Facturación deflactada por el IPC (Base Sep-2024).
  - `Ventas_USD_Blue`: Conversión a dólares blue diarios con `LOOKUPVALUE`.

## 📁 Archivos del Repositorio
- `archivopowebi.pbix`: Reporte interactivo de Power BI.
- `informe.pdf`: Informe completo del Trabajo Práctico.
- Archivos de datos originales (`.xlsx`, `.csv`, `.json`).
