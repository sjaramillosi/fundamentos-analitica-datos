# Fundamentos de analítica de datos

Portafolio de los laboratorios y proyectos que desarrollé en el curso de fundamentos de
analítica de datos (semestre 2026-2) de la Universidad Nacional de Colombia.

El repositorio recorre el ciclo de un proyecto de datos: leer y validar fuentes, limpiar,
proteger la privacidad, consultar con SQL, analizar con pandas y construir modelos de
aprendizaje automático. Cada actividad incluye pruebas automáticas con `pytest`.

**Herramientas:** Python, pandas, NumPy, SQL (SQLite), scikit-learn, matplotlib, seaborn,
NLTK, SciPy, pytest, Git y GitHub Actions.

## Laboratorios

| Actividad | Qué se hace | Herramientas |
|---|---|---|
| [L101 – Python básico](L101_python_basico) | Preguntas sobre un archivo tabular resueltas solo con Python (listas, diccionarios, ciclos). | Python, `csv` |
| [L102 – Pandas](L102_pandas) | Consultas, agrupaciones y uniones sobre tres tablas. | pandas |
| [L103 – Ingestión de texto plano](L103_ingestion_de_texto_plano) | Conversión de un reporte de texto con formato libre en una tabla. | pandas |
| [L104 – Ingestión de texto en directorios](L104_ingestion_de_texto_en_directorios) | Construcción de datasets de entrenamiento y prueba a partir de carpetas de archivos de texto etiquetados. | pandas, `os` |
| [L105 – Validación de datos](L105_validacion_de_datos) | Reporte de calidad de datos de ventas (faltantes, formatos, duplicados) antes de limpiar. | pandas, JSON |
| [L106 – Limpieza de solicitudes de crédito](L106_limpieza_de_solicitudes_de_credito) | Limpieza de texto, fechas y montos, y eliminación de duplicados. | pandas |
| [L107 – Limpieza de campañas](L107_limpieza_de_campanas) | Unión de varios archivos de una campaña bancaria y separación en tablas de cliente, campaña y economía. | pandas |
| [L108 – k-anonimato de asegurados](L108_k_anonimato_de_asegurados) | Publicación de datos de seguros con k-anonimato y reporte de privacidad. | pandas |
| [L109 – SQL con SQLite](L109_sql_con_sqlite3) | Consultas SQL con agrupaciones, filtros y uniones. | SQL, SQLite |
| [L110 – Rentabilidad de ventas](L110_rentabilidad_de_ventas) | Rentabilidad por segmento y efecto de los descuentos en una tienda. | pandas |
| [L111 – Demoras ajustadas por horario](L111_demoras_ajustadas_por_horario) | Comparación de aerolíneas ajustando sus demoras por la hora de operación. | pandas |
| [L112 – Cohortes de clientes](L112_cohortes_de_clientes) | Retención de clientes por cohorte mensual y mapa de calor. | pandas, seaborn |
| [L113 – Tiempos de respuesta PQRS](L113_tiempos_de_respuesta_pqrs) | Tiempos de respuesta en días hábiles por canal, año y día de entrada. | pandas, NumPy |

## Proyectos

| Actividad | Qué se hace | Herramientas |
|---|---|---|
| [P001 – Hola mundo](P001_hola_mundo) | Primera entrega: configuración del entorno y funciones simples verificadas con pruebas. | Python, pytest |
| [P100 – MapReduce: conteo de palabras](P100_mapreduce_word_count) | Conteo de palabras con las fases map, shuffle/sort y reduce. | Python |
| [P101 – Manejo del editor](P101_manejo_editor) | El conteo de palabras de P100 reescrito desde el editor, con rutas `pathlib`. | Python, VS Code |
| [P102 – CSV a JSON](P102_csv2json) | Exportación de un archivo CSV de conductores a JSON. | Python, `json` |
| [P103 – Conductores con pandas](P103_drivers_pandas) | Resumen de horas y millas por conductor y top 10 en gráfica. | pandas, matplotlib |
| [P104 – Conductores con SQLite](P104_drivers_sqlite) | El mismo análisis anterior resuelto con SQL. | SQLite, pandas |
| [P105 – Conductores con ChatGPT](P105_drivers_chatgpt) | El mismo análisis con código generado por IA y verificado contra P103. | pandas |
| [P106 – Limpieza con pandas](P106_limpieza_pandas) | Limpieza de una tabla de ventas: nombres, fechas, monedas, pesos y duplicados. | pandas, expresiones regulares |
| [P107 – Limpieza con SQL](P107_limpieza_sql) | La misma limpieza resuelta con SQL. | SQLite, pandas |
| [P108 – Anonimización con pandas](P108_anonimizacion_pandas) | Seudonimización y generalización de perfiles de clientes, con prueba de reidentificación. | pandas, `hashlib` |
| [P109 – Anonimización con SQL](P109_anonimizacion_sql) | La misma anonimización resuelta con SQL. | SQLite |
| [P200 – Regresión básica](P200_regresion_basica) | Predicción del consumo de combustible (MPG) con regresión lineal, términos no lineales y redes neuronales. | scikit-learn |
| [P201 – Clasificación de imágenes](P201_clasificacion_basica_imagenes) | Clasificación de dígitos escritos a mano y análisis de la incertidumbre de cada predicción. | scikit-learn, matplotlib |
| [P202 – Tokenización](P202_tokenizacion) | Tokenización, *stopwords* y *stemming* de resúmenes científicos, y matriz documento-término. | NLTK, scikit-learn, SciPy |
| [P203 – Clasificación de texto](P203_clasificacion_basica_texto) | Clasificación del sentimiento (positivo, negativo o neutral) de frases de noticias financieras. | scikit-learn |
| [P204 – Clasificación numérica](P204_clasificacion_basica_numerica) | Diagnóstico de tumores (benigno o maligno) con regresión logística y una red neuronal. | scikit-learn |
| [P205 – Priorización con probabilidades](P205_priorizacion_con_probabilidades) | Calibración de probabilidades de incumplimiento, umbrales de revisión y comparación entre grupos. | pandas, scikit-learn |
| [P206 – Clustering de demanda](P206_clustering_demanda) | Agrupación de perfiles diarios de demanda de energía con K-Means y selección por silueta. | scikit-learn, matplotlib |

Las carpetas P207, P300–P302 y P400–P402 corresponden a actividades del curso que no
desarrollé.

## Estructura de cada actividad

```
Lxxx_nombre/ o Pxxx_nombre/
├── data/          datos de entrada
├── src/           solución en scripts (.py o .sql)
├── notebooks/     solución en notebooks (proyectos P2xx)
├── submission/    resultados generados
└── tests/         pruebas automáticas
```

## Cómo ejecutar

### MacOS y Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
source setup.sh
```

### Windows

```bash
python3 -m venv .venv
.venv\Scripts\activate
setup
```

### Pruebas

```bash
pytest
```
