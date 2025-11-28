# 📘 README – Proyecto de Análisis de Ventas con Python, PostgreSQL y Power BI
### 📌 Autora: **Nadine Isabel Castillo**
### 🗂 Historias de Usuario desarrolladas: **HU1 – HU5**

# 🧩 Descripción del Proyecto
Este proyecto consiste en el análisis completo de un dataset de ventas, aplicado mediante un flujo analítico real que incluye:
- Limpieza y transformación de datos en Python  
- Normalización y validación de la calidad de datos  
- Creación de modelo estrella en PostgreSQL  
- Conexión directa entre Power BI ↔ PostgreSQL  
- Construcción de dashboards interactivos con KPIs y visualizaciones avanzadas  

---

# 🟣 Historia de Usuario 1 – Conexión y carga de datos desde PostgreSQL
### 🎯 Objetivo
Como analista, quiero conectarme a una base PostgreSQL para almacenar los datos procesados desde Python.

### 🔧 Tareas realizadas
- Configurar conexión mediante SQLAlchemy y psycopg2  
- Leer archivo CSV original  
- Ajustar encabezados  
- Crear base de datos `ventas_db`  
- Exportar DataFrame → tabla `ventas`  

---

# 🟣 Historia de Usuario 2 – Limpieza y normalización de datos
### 🎯 Objetivo
Limpiar y estructurar los datos para asegurar integridad y consistencia.

### 🔧 Tareas realizadas
- Eliminar duplicados  
- Manejar valores nulos  
- Normalizar texto (ciudad, tipo de producto, cliente, canal)  
- Detectar valores inconsistentes  
- Reporte de calidad de datos  

---

# 🟣 Historia de Usuario 3 – Análisis Exploratorio de Datos (EDA)
### 🎯 Objetivo
Analizar tendencias, patrones y comportamientos de ventas.

### 🔧 Tareas realizadas
- Métricas descriptivas  
- Análisis temporal  
- Top 5 productos  
- Ventas por categoría  
- Visualizaciones con Matplotlib y Seaborn  

---

# 🟣 Historia de Usuario 4 – Modelo Estrella y conexión Power BI ↔ PostgreSQL
### 🎯 Objetivo
Construir un modelo de datos profesional y listo para análisis.

### 🔧 Tareas realizadas
- Fact_Ventas  
- Dim_Fecha, Dim_Producto, Dim_Cliente, Dim_Ciudad, Dim_TipoVenta  
- Relaciones 1:*  
- Validación de integridad  

---

# 🟣 Historia de Usuario 5 – Dashboard en Power BI
### 🎯 Objetivo
Construir un tablero interactivo con KPIs y visualizaciones clave.

### 🔧 Tareas realizadas
- Comparativa ventas año actual vs anterior  
- Top 5 productos  
- Top 10 ciudades  
- Mapa geográfico  
- Ventas por tipo de cliente y tipo venta  
- KPIs mensuales  
- Segmentadores dinámicos  
- Publicación y documentación  

---

# 🧮 Métricas DAX principales
```
Total Ventas = SUM(Fact_Ventas[Total_Pagado])

Ventas Año Anterior =
CALCULATE([Total Ventas], SAMEPERIODLASTYEAR(Dim_Fecha[Date]))

% Crecimiento =
DIVIDE([Ventas Año Actual] - [Ventas Año Anterior], [Ventas Año Anterior])

Ticket Promedio = AVERAGE(Fact_Ventas[Total_Pagado])
```

---

# 🗂 Archivos del Proyecto
```
📁 Proyecto_Ventas
├── README.md
├── HU1_Conexion_PostgreSQL.ipynb
├── HU2_Limpieza_Normalizacion.ipynb
├── HU3_EDA_Analisis.ipynb
├── HU4_Modelo_Estrella.pbix
├── HU5_Dashboard_Ventas.pbix
├── ventas_original.csv
└── ventas_limpia.csv
```

---

# 🏁 Conclusión Final
Este proyecto demuestra el ciclo completo de análisis moderno:  
Python → PostgreSQL → Power BI → Dashboard.

Trabajo desarrollado mediante metodología ágil con 5 historias de usuario.

