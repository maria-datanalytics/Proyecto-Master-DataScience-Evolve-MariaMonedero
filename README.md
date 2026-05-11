# Enterprise Financial & Operational Intelligence Platform

## Descripción del proyecto
Solución analítica end-to-end orientada al reporting ejecutivo mediante una arquitectura de medallones (Bronze/Silver/Gold) desarrollada en Microsoft Fabric y consumida desde dashboards ejecutivos en Power BI para la toma de decisiones estratégicas.

## Tecnologías utilizadas
Microsoft Fabric · PySpark Notebooks · Lakehouse · Medallion Architecture · Power BI · DAX · Data Modeling · Star Schema · Executive Dashboard Design

## Estructura del Proyecto
```text
enterprise-financial-analytics/
│
├── data/
│   └── enterprise_financial_operations_raw.csv
│
├── notebooks/
│   ├── nb_01_raw_to_bronze.ipynb
│   ├── nb_02_bronze_to_silver.ipynb
│   └── nb_03_silver_to_gold.ipynb
│
├── powerbi/
│   ├── Enterprise_Financial_Analytics.pbix
│   └── screenshots/
│
├── docs/
│   └── architecture_overview.png
│
└── README.md
```

## Arquitectura del proyecto
```text
CSV RAW
enterprise_financial_operations_raw.csv
        ↓
BRONZE LAYER
bronze_fact_operations_raw
        ↓
SILVER LAYER
silver_fact_operations
        ↓
GOLD LAYER
gold_fact_operations
gold_dim_region
gold_dim_department
gold_dim_business_unit
gold_dim_risk
gold_dim_date
        ↓
POWER BI
Executive Analytics Dashboard
```

## Star Schema
Fact table:
- gold_fact_operations

Dimension tables:
- gold_dim_region
- gold_dim_department
- gold_dim_business_unit
- gold_dim_risk
- gold_dim_date

## KPIs implementados en DAX
| Categoría | KPI | Descripción |
|---|---|---|
| Financial | Total Revenue | Ingresos totales generados |
| Financial | Total Profit | Beneficio total operativo |
| Financial | Profit Margin % | Margen de beneficio sobre ingresos |
| Financial | Total Operating Cost | Coste operativo total |
| Operational | Cost Efficiency Ratio | Ratio de eficiencia coste/ingreso |
| Operational | Average Productivity Score | Productividad media operativa |
| Operational | Hidden Operational Costs | Costes ocultos operativos |
| Risk | High Risk Operations | Número de operaciones de alto riesgo |
| Risk | High Risk Operations % | Porcentaje de operaciones de alto riesgo |
| Risk | Average Risk Score | Nivel medio de riesgo operativo |
| Variance | Budget Variance | Desviación respecto al presupuesto |
| Variance | Forecast Variance | Desviación respecto a previsiones |

## Ejecución del proyecto
1. Cargar el dataset raw en el Lakehouse de Microsoft Fabric.
2. Ejecutar los notebooks: nb_01_raw_to_bronze → nb_02_bronze_to_silver → nb_03_silver_to_gold
3. Conectar Power BI al Lakehouse utilizando el Import Mode.
4. Configurar el modelo estrella y las medidas DAX.

## Resultados principales
- Arquitectura Medallion escalable para reporting corporativo.
- Dashboard ejecutivo con KPIs financieros, operacionales y de riesgo.
- Modelo analítico optimizado para toma de decisiones estratégicas.
- Storytelling de negocio orientado a eficiencia, costes y monitorización operativa.

## Business Value
La plataforma centraliza el reporting financiero y operacional en un único modelo analítico, facilitando la monitorización ejecutiva mediante KPIs estratégicos, análisis de eficiencia, control de riesgos operativos y detección de costes ocultos. 

## Autor
María Monedero Fernández

Proyecto académico desarrollado durante el Máster en Data Science & Artificial Intelligence de Evolve 
