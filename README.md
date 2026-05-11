# Enterprise Financial & Operational Intelligence Platform

## Descripción del proyecto
Solución analítica end-to-end orientada al reporting ejecutivo financiero y operacional mediante una arquitectura automatizada de medallones (Bronze/Silver/Gold) desarrollada en Microsoft Fabric y consumida desde dashboards ejecutivos en Power BI para la toma de decisiones estratégicas.

## Objetivo del proyecto
Transformar datos empresariales "raw" en información estratégica para la toma de decisiones ejecutivas automatizando: 
- Ingesta de datos
- Limpieza y transformación de datos
- Modelado analítico
- Visualización de KPIs financieros y operacionales

## Tecnologías utilizadas
### Data Engineering & Analytics
- Microsoft Fabric
- PySpark Notebooks
- Lakehouse
- Medallion Architecture

### Business Intelligence
- Power BI
- DAX
- Data Modeling
- Executive Dashboard Design

### Arquitectura de datos
- Bronze Layer
- Silver Layer
- Gold Layer
- Star Schema
- Fact and Dimension Modeling

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

## Pipeline del proyecto
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

## Puntos de análisis
1. Rentabilidad
2. Desviaciones presupuestarias
3. Productividad
4. Riesgo operativo
5. Costes ocultos asociados a ineficiencias operacionales

## Solución diseñada con enfoque executive/corporate orientado al:
1. Control financiero
2. Reporting ejecutivo
3. Análisis de eficiencia operativa
4. Detección de riesgos y costes ocultos
5. Soporte para la toma de decisiones

## Ejecución del proyecto
1. Clonar el repositorio.
2. Abrir Microsoft Fabric: crear el Workspace, el lakehouse y los 3 notebooks.
3. Cargar el dataset raw: enterprise_financial_operations_raw.csv a los files del Lakehouse.
4. Ejecutar los Notebooks en orden: nb_01_raw_to_bronze → nb_02_bronze_to_silver → nb_03_silver_to_gold para generar las tablas de dimensiones y facts. 
5. Conectar el Lakehouse desde Power BI utilizando Import Mode.
6. Configurar el modelo estrella con relaciones one-to-many de dirección única hacia la tabla gold_fact_operations.
7. Implementar las siguientes medidas DAX: Financial KPIs (Total Revenue, Total Profit, Profit Margin % y Total Operating Cost), Operational KPIs (Cost Efficiency Ratio, Average Productivity Score, Hidden Operational Costs), Risk KPIs (High Risks Operations, High Risk Operations % y Average Risk Score) y Variance Analysis (Budget Variance y Forecast Variance).

## Modelo estrella
Modelo dimensional optimizado para el consumo analítico en Power BI compuesto por:
- Tabla de hechos central: gold_fact_operations
- Dimensiones analíticas: gold_dim_region, gold_dim_department, gold_dim_business_unit, gold_dim_risk y gold_dim_date

## Resultados principales
- Arquitectura medallón separada por capas con un modelo escalable para reporting corporativo. 
- Dashboard ejecutivo con visión financiera global, análisis operacional, monitorización del riesgo, KPIs ejecutivos y navegación corporativa.
- Storytelling de negocio enfocado en eficiencia financiera, control de costes, desviaciones presupuestarias, productividad y soporte a decisiones estratégicas.

## Enfoque del proyecto
- Arquitectura moderna de datos
- Gobierno y Modelado analítico
- Diseño ejecutivo del dashboard
- Storytelling financiero
- Experiencia orientada al negocio

## Business Value
La plataforma permite centralizar el reporting financiero y operacional en un único modelo analítico, reduciendo la fragmentación de la información y facilitando la monitorización ejecutiva mediante KPIs estratégicos, análisis de eficiencia y control de riesgos operativos.

## Autor
María Monedero Fernández

Proyecto académico desarrollado durante el Máster en Data Science & Artificial Intelligence de Evolve 
