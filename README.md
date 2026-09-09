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
10_dashboard_analisis_comercial_ACRE/
│
├── Datasets/                                ← Datos fuente
│   ├── dim_propiedades.csv                  # 8,000 registros de propiedades · 8 columnas
│   ├── dim_clientes.csv                     # 3,500 registros de clientes · 4 columnas
│   └── hecho_ventas_propiedades.csv         # 8,500 transacciones de venta · 10 columnas
│
├── exports/                                ← Generado al ejecutar data wrangling
│   ├── Andes_Capital_RE_2023_2024.xlsx      # Dataset consolidado para Power BI
│
├── notebooks/
│   ├── S11_P10 Proyecto_InmobiliarioGrupoAndes.ipynb  # ETL · KPIs base · Análisis · estadística · conclusiones
│
├── dashboard/
│   └── S11_P10_Analisis_Comercial_ACRE.pbix           # Dashboard Power BI · 3 páginas · medidas DAX
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
## Estructura del dashboard
**🖥️ Vista 1: Overview ejecutivo**<br>
Responde a la pregunta: ¿Cómo está el negocio en general?<br>

En esta vista se ofrece una lectura rápida del desempeño global.<br>
Se aplicaron principios de diseño de dashboards como:<br>
- Jerarquía visual (KPIs principales en la parte superior, detalle debajo).
- Preatención (color y tamaño para dirigir la mirada a lo más relevante).
- Alineación y agrupación de elementos relacionados.
- Minimalismo visual (evitar sobrecarga de gráficos).<br>
De modo que un directivo pueda entender la situación en pocos segundos.<br><br>

Se incluyó información como:<br>
- Métricas clave de desempeño (ventas, ganancia, volumen, etc.).
- Evolución del negocio a lo largo del tiempo.
- Comparaciones generales entre geografías o segmentos.
- Elementos que resuman el estado actual del negocio<br>
👉 Se priorizó síntesis y claridad sin demasiados gráficos.<br><br>

**🔎 Vista 2: Análisis detallado**<br>
Responde a la pregunta: ¿Dónde están las diferencias, patrones u oportunidades?<br>
Aquí se desglosa un análisis más profundo que permite explorar causas y detectar insights.<br><br>

Se incluyen: <br>
- Comparaciones entre categorías, segmentos o regiones.
- Visuales que permiten filtrar o profundizar
- Elemento de detalle (tabla) para profundizar en los datos<br>
👉 Esta vista facilita la exploración y el diagnóstico, no sólo muestra totales. Su objetivo es brindar profundidad analítica y soporte a decisiones.
---

## Cómo reproducir el análisis

**1. Revisión del notebook**<br>
Jupyter notebook: **[notebooks/S11_P10 Proyecto_InmobiliarioGrupoAndes.ipynb](https://github.com/marisolmtzp/10_dashboard_analisis_comercial_ACRE/blob/27c85dfebb263785fa8db2c3e526a91af37278bc/notebooks/S11_P10%20Proyecto_InmobiliarioGrupoAndes.ipynb)**

**2. Power BI**<br>
Descargar el dashboard y abrirlo en Power BI: **[dashboards/S11_P10_Analisis_Comercial_ACRE.pbix](https://github.com/marisolmtzp/10_dashboard_analisis_comercial_ACRE/tree/578f0806d453d2d0dd9ee1a15546db6d909f000f/dashboards)**<br>
Conectar dashboard a la fuente de datos limpia: **[exports/Andes_Capital_RE_2023_2024.xlsx](https://github.com/marisolmtzp/10_dashboard_analisis_comercial_ACRE/tree/84e0940c20bae506b1d679c04503eec56d594b4f/exports)**

---

*Marisol Martínez Pulgarín · Data Analyst | Business Analyst | BI Developer*  · 
*[LinkedIn](https://www.linkedin.com/in/marisolmtzp/) · [GitHub](https://github.com/marisolmtzp) · [Portafolio](https://marisolmtzp.github.io)*

