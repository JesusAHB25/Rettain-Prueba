# Análisis de Campañas de Email Marketing - Prueba Técnica Rettain

Este repositorio contiene la solución técnica integral para el análisis de rendimiento de campañas de email marketing. El proyecto abarca desde el procesamiento crudo de datos con Python hasta la generación de insights estratégicos de negocio.

## 🚀 Resumen del Proyecto
El objetivo principal es identificar los patrones de comportamiento de los usuarios (aperturas, clics y compras) para optimizar el calendario de envíos y maximizar el **Revenue per Recipient (RPR)**.

### 📊 [Ver Reporte Interactivo y Dashboard en Google Sheets](https://docs.google.com/spreadsheets/d/1xan9sYGSBXpzL3zQYJDPU6s0X9hFXrPGH5jBVL_5sS4/edit?usp=sharing)
*Nota: El reporte en Sheets contiene las visualizaciones finales, dashboards de KPI y el desglose detallado de las 8 preguntas requeridas.*


## 🛠️ Herramientas y Metodología
- **Python (Pandas & Numpy):** Utilizados para el robusto pipeline de limpieza y transformación.
- **Ingeniería de Datos:** - Normalización de tipos de datos monetarios y limpieza de caracteres especiales.
    - Procesamiento de series temporales para extraer `Day_of_Week` e intervalos de 1 hora.
    - Manejo de excepciones matemáticas (divisiones por cero) para asegurar la integridad de las métricas.
- **Google Sheets:** Plataforma de BI para la visualización de datos y comunicación de hallazgos.


## 🧠 Desafíos Técnicos Resueltos
1. **Normalización de Monedas:** Se eliminaron símbolos y formatos inconsistentes para permitir cálculos aritméticos precisos.
2. **Sincronización Temporal:** Conversión de timestamps a objetos datetime con normalización UTC para agrupar campañas por ventanas horarias de 60 minutos.
3. **Métricas de Eficiencia:** Desarrollo de la métrica RPR como KPI principal para eliminar el sesgo producido por el volumen de destinatarios en el Revenue total.


## 💡 Hallazgos Estratégicos (Insights)
- **Ventana Dorada:** El domingo a las 17:00 presenta el mayor potencial de retorno (**$0.74 RPR**).
- **Pico Operativo:** El mayor volumen de transacciones ocurre entre las 12:00 y 13:00 (hora de almuerzo).
- **Segmentación:** Los viernes son el motor de adquisición de nuevos clientes, mientras que los sábados son la clave para la retención de clientes recurrentes.


## 📂 Estructura del Repositorio
```text
├── data/
│   └── Prueba Analisis de Datos - Rettain - Limpio.csv  # Dataset procesado
├── notebooks/
│   └── Limpieza_del_DF.ipynb                            # Script de limpieza en Python
├── output/                                              # Datasets resultantes por pregunta
│   ├── p1.csv, p2.csv, p3_rpr.csv y .csv de origen      # Métricas de Rentabilidad
│   ├── p456.csv                                         # Métricas de Engagement
│   └── p78.csv                                          # Métricas de Segmentación
└── README.md
```
