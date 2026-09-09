# Dashboard - Análisis de desempeño comercial 2024-2025 <br>Andes Retail Group
![Power BI](https://img.shields.io/badge/Power%20BI-PowerQuery-F2C811?style=flat&logo=powerbi&logoColor=black)
![Power BI](https://img.shields.io/badge/Power%20BI-StarSchema-4B8BBE?style=flat&logo=powerbi&logoColor=black)
![Power BI](https://img.shields.io/badge/Power%20BI-DAX-F2C811?style=flat&logo=powerbi&logoColor=black)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?style=flat&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![SCQA](https://img.shields.io/badge/SCQA-FF6F00?style=flat)
![EDA](https://img.shields.io/badge/EDA-4B8BBE?style=flat)
![Segmentación](https://img.shields.io/badge/Segmentaci%C3%B3n_Clientes-4B8BBE?style=flat)
---
## Contexto y problema de negocio
La empresa Andes Retail Group es una empresa de retail con operaciones en Perú, Chile y Colombia. La empresa comercializa productos en cuatro categorías:<br><br>
🖥️ Electrónica<br>
👕 Ropa<br>
⚽ Deportes<br>
🏠 Hogar<br><br>
Su dirección ejecutiva necesita un dashboard interactivo que permita entender el desempeño comercial de los años 2024–2025. Actualmente, la información está dispersa en datos transaccionales y no existe una visión clara que permita responder preguntas estratégicas sobre ventas, rentabilidad y comportamiento de clientes.

👉 La misión del proyecto es transformar estos datos desordenados en un dashboard que presente la información visual, clara y accionable.

**💡 Preguntas del negocio**
El dashboard ayuda a responder preguntas como:
> *¿Cómo ha evolucionado el ingreso total entre 2024 y 2025?*<br>
> *¿Qué segmentos de clientes aportan mayor ingreso y rentabilidad?*<br>
> *¿Qué categorías de producto tienen mayor impacto en el negocio?*<br>
> *¿Existen diferencias relevantes entre países o regiones?*<br>
> *¿Qué patrones temporales se observan a lo largo del año?*<br>
> *¿Dónde podrían existir oportunidades de mejora comercial?*<br>

## 🎯 Funcionalidades implementadas
- Conexión y validación de un **dataset transaccional**.
- **Preparación de datos** para el análisis.
- Diseño de dashboards aplicando **principios de diseño visual profesional**.
- Construcción de **visualizaciones claras que responden preguntas de negocio**.
- Implementación de **filtros e interacciones que permiten exploración dinámica**.
- Narrativa estratégica usando el **modelo SCQA**.
- **Presentación de hallazgos de forma ejecutiva** en dashboard y de forma asíncrona.

## 🛠️ Herramientas del proyecto
- Power BI Desktop o Tableau
- Visualizaciones nativas (barras, líneas, mapas, tarjetas KPI)
- Modelo de narrativa SQCA

## 📂 Dataset del proyecto
El proyecto utiliza una tabla de transacciones de ventas del negocio retail Andes Retail Group correspondientes a los años 2024–2025.

**Andes_Retail_Group_2024_2025.xlsx : Cada fila representa un pedido individual, incluyendo información del cliente, ubicación geográfica, categoría de producto y métricas financieras como ingresos y costo.**<br>
👉 Este dataset permitirá analizar desempeño comercial, rentabilidad y comportamiento temporal del negocio.<br>

<sub>

| Columna | Tipo de dato | Descripción | Ejemplo |
|--------|--------|------------------|------------------|
| ID_Pedido | Numérico (int) | Identificador único del pedido | 1 |
| Fecha_Pedido | Fecha | Día en que se realizó la venta | 2025-10-29 |
| Estación | Categórica | Temporada del año según el hemisferio sur: Primavera, Verano, Otoño, Invierno | Primavera |
| ID_Cliente | Categórica | Identificador único del cliente | C8382 |
| Segmento_Cliente | Categórica | Tipo de cliente según valor comercial | Estándar |
| Región | Categórica | Región geográfica dentro del país | Sur |
| País | Categórica | País donde se realizó la venta | Colombia |
| Categoría_Producto | Categórica | Tipo de producto vendido | Hogar |
| Unidades_Vendidas | Numérico (int) | Cantidad de unidades vendidas | 7 |
| Precio_Unitario | Numérico (decimal) | Precio por unidad del producto | 67 |
| Ingresos | Numérico (decimal) | Total vendido (precio × unidades) | 469 |
| Costo | Numérico (decimal) | Costo asociado a la venta | 325.44 |

</sub>








## Estructura del proyecto
```
09_dashboard_desempeno_comercial_ARG/
│
├── Datasets/                                ← Datos fuente
│   └── Andes_Retail_Group_2024_2025.xlsx    # 5,000 registros de venta · 12 columnas
│
├── exports/                                ← En este caso las modificaciones al dataset se realizaron en Power BI
│   ├── Andes_Capital_RE_2023_2024.xlsx      # Dataset consolidado luego de cargarse a Power BI
│
├── notebooks/
│   ├── S10_P09 Proyecto_Desempeno_Comercial_ARG.ipynb  # Contexto · KPIs base · Análisis · estadística · conclusiones
│
├── dashboard/
│   └── S10_P09_Desempeno_Comercial_ARG.pbix           # Dashboard Power BI · 2 páginas · columnas/medidas DAX
│
└── README.md
```

## 🔄 Flujo general del proyecto (Guía paso a paso)
El proceso está documentado en el Jupyter Notebook del proyecto que incluye los detalles sobre:

| Pasos | Acción | Resultado |
|--------|------------------|------------------|
| 1. Conexión y exploración | Importación del dataset y revisión de tipos de datos, columnas y métricas clave | Comprensión inicial del negocio y estructura del dataset |
| 2. Preparación de datos | Validación de tipos, creación de columnas necesarias, revisión de consistencia | Dataset limpio y listo para análisis |
| 3. Aplicación de principios de diseño visual | Definición de layout, jerarquía visual, colores y estructura antes de la creación de visualizaciones | Dashboard claro y profesional |
| 4. Creación de visualizaciones efectivas | Diseño de dos vistas: Vista General (overview) y Vista Detalle (análisis específico) | Visión ejecutiva + análisis profundo |
| 5. Filtros e interacciones | Implementación de filtros y configuración de interacciones entre gráficos | Exploración dinámica del negocio |
| 6. Narrativa con modelo SCQA | Construcción de la historia dentro del dashboard y muestra de comunicación de hallazgos vía medios  asíncronos como Slack | Insight estratégico claro y accionable |

---

## 📊 Estructura del dashboard

#### 🖥️ Vista 1: Overview ejecutivo
**¿Cómo está el negocio en general?**
Lectura rápida del desempeño global, aplicando jerarquía visual, preatención, alineación/agrupación y minimalismo visual.
- Métricas clave (ventas, ganancia, volumen)
- Evolución temporal del negocio
- Comparaciones entre geografías o segmentos
- Estado actual resumido

👉 Síntesis y claridad, sin sobrecarga de gráficos.

#### 🔎 Vista 2: Análisis detallado
**¿Dónde están las diferencias, patrones u oportunidades?**
Análisis profundo para explorar causas y detectar insights.
- Comparaciones entre categorías, segmentos o regiones
- Visuales con filtros para profundizar
- Tabla de detalle

👉 Profundidad analítica y soporte a decisiones.

---

### 💭 Reflexión personal

> **Lo que más reforcé en este proyecto:** diseño visual y comunicación ejecutiva del dashboard.<br>
> En este proyecto puse especial énfasis en que el diseño no fuera solo estético, sino funcional: trabajé la jerarquía visual para que los KPIs principales resaltaran de inmediato, cuidé que los colores reforzaran el mensaje (y no solo decoraran), y evité la sobrecarga de gráficos para que cada visual tuviera un propósito claro dentro de una secuencia lógica. La narrativa completa se construyó bajo la estructura SCQA, buscando que el dashboard no sólo mostrara datos, sino que contara una historia con sentido de negocio.
> ***Esto me confirmó que la calidad de un dashboard no se mide por cuántos gráficos tiene, sino por qué tan rápido y con qué claridad comunica un hallazgo a quien toma decisiones.***


## Cómo reproducir el análisis

**1. Revisión del notebook**<br>
Jupyter notebook (guía de trabajo para construir el dashboard, aquí se documentaron decisiones, métricas y hallazgos): **[notebooks/S10_P09 Proyecto_Desempeno_Comercial_ARG.ipynb](https://github.com/marisolmtzp/09_dashboard_desempeno_comercial_ARG/blob/7f2bdd365b113cf77d6c23bfd6b97caa0d20bde0/notebooks/S10_P09%20Proyecto_Desempeno_Comercial_ARG.ipynb)**

**2. Power BI**<br>
Descargar el dashboard y abrirlo en Power BI: **[dashboards/S10_P09_Desempeno_Comercial_ARG.pbix](https://github.com/marisolmtzp/09_dashboard_desempeno_comercial_ARG/blob/1fde0a06448e0bcfbce8d2914b59e43d275c1bc2/dashboards/)**<br>
Conectar dashboard a la fuente de datos limpia: **[exports/Andes_Retail_Group_2024_2025.xlsx](https://github.com/marisolmtzp/09_dashboard_desempeno_comercial_ARG/blob/97ae7724744d354136ad00e2bbc5a4d5f0096397/exports/)**

---

*Marisol Martínez Pulgarín · Data Analyst | Business Analyst | BI Developer*  · 
*[LinkedIn](https://www.linkedin.com/in/marisolmtzp/) · [GitHub](https://github.com/marisolmtzp) · [Portafolio](https://marisolmtzp.github.io)*

