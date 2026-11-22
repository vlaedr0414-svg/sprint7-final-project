# sprint7-final-project
Analizar la información de clientes y registros de uso de ConectaTel para identificar problemas de calidad de datos, segmentar usuarios por edad y nivel de uso, detectar patrones de comportamiento y generar recomendaciones de negocio basadas en evidencia
Análisis de Clientes y Patrones de Uso - ConectaTel
📌 Objetivo del proyecto
Analizar la información de clientes y registros de uso de ConectaTel para identificar problemas de calidad de datos, segmentar usuarios por edad y nivel de uso, detectar patrones de comportamiento y generar recomendaciones de negocio basadas en evidencia.
Datasets utilizados
users.csv
Contiene información de los clientes:

user_id
age
city
plan
reg_date
usage.csv
Contiene información de uso de los servicios:

user_id
date
type
duration
length
🔧 Proceso de análisis
1. Exploración inicial
Se revisó la estructura de los datasets para identificar:

Valores faltantes
Valores inválidos (sentinels)
Tipos de datos incorrectos
Fechas fuera de rango
2. Limpieza de datos
Acciones realizadas:

Reemplazo de valores -999 en age por la mediana.
Conversión de valores ? en city a nulos.
Conversión de columnas de fecha al tipo datetime.
Corrección de registros con fechas fuera de rango (año 2026).
Validación de valores faltantes en variables de uso.
3. Análisis exploratorio
Se analizaron:

Distribución de edades.
Distribución de planes contratados.
Cantidad de mensajes por usuario.
Cantidad de llamadas por usuario.
Minutos totales consumidos.
4. Detección de outliers
Se utilizaron:

Histogramas.
Boxplots.
Método IQR.
Variables evaluadas:

age
cant_mensajes
cant_llamadas
cant_minutos_llamada
5. Segmentación de clientes
Segmentación por uso
Bajo uso
Uso medio
Alto uso
Segmentación por edad
Joven (< 30 años)
Adulto (30-59 años)
Adulto Mayor (60+ años)
📈 Hallazgos principales
Se detectaron valores inválidos y fechas fuera de rango que fueron corregidos.
La mayoría de los usuarios presenta niveles de uso moderados.
Existe un grupo reducido de usuarios intensivos con altos consumos de minutos y llamadas.
Los outliers detectados representan comportamientos reales y fueron conservados.
Los usuarios de alto uso representan una oportunidad importante para estrategias de fidelización y upselling.
💡 Recomendaciones
Crear planes premium para usuarios intensivos.
Diseñar campañas específicas para usuarios de uso medio.
Implementar promociones segmentadas por edad.
Mantener monitoreo continuo de clientes con alto consumo.
Fortalecer los controles de calidad de datos.
▶️ Cómo ejecutar el proyecto
En Google Colab
Abrir el notebook .ipynb.
Cargar los datasets necesarios.
Ejecutar todas las celdas en orden.
Revisar las visualizaciones y conclusiones generadas.
En Jupyter Notebook
jupyter notebook
Abrir el archivo .ipynb y ejecutar todas las celdas secuencialmente.

📁 Estructura sugerida del repositorio
telecom-analysis/
│
├── data/
│   ├── users.csv
│   └── usage.csv
│
├── notebooks/
│   └── conectatel_analysis.ipynb
│
├── README.md
│
└── requirements.txt
👤 Autor
Luis Rubén Yañez Ortega

Proyecto de análisis exploratorio, limpieza de datos y segmentación de clientes para ConectaTel.
