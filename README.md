📊 Observatorio Integrado del Gas Natural – Colombia
Dashboard analítico en Power BI | Producción · Demanda · Regalías
El Observatorio Integrado del Gas Natural es una plataforma diseñada para analizar el comportamiento histórico y futuro del mercado gasífero colombiano.
Permite estudiar el estado actual del sistema energético, identificar tendencias críticas de regalías, proyectar demanda, evaluar producción agregada por operador y explorar la distribución territorial del consumo y generación de ingresos.
Este proyecto consolida datos oficiales nacionales mediante procesos ETL en Microsoft Fabric, integrados en un modelo semántico que posteriormente alimenta un dashboard interactivo desarrollado en Power BI.

ACCESO INFORME: https://app.powerbi.com/view?r=eyJrIjoiMmY1YjFhNzAtYTU5OS00MmUxLWE5NTQtZTI0MjJhOGFhMDU2IiwidCI6ImY1OTI1YWQ5LTM0ZjUtNDM2OS1hZTFiLTA5ZDYyODI2NjFmMyJ9

<iframe title="informe-produccion _demanda_regalias_gas-natural" width="1024" height="1060" src="https://app.powerbi.com/view?r=eyJrIjoiMmY1YjFhNzAtYTU5OS00MmUxLWE5NTQtZTI0MjJhOGFhMDU2IiwidCI6ImY1OTI1YWQ5LTM0ZjUtNDM2OS1hZTFiLTA5ZDYyODI2NjFmMyJ9" frameborder="0" allowFullScreen="true"></iframe>
________________________________________


🌐 Arquitectura General del Proyecto
El flujo de desarrollo del observatorio consta de:
📥 Recolección de datos oficiales (UPME · MinMinas · ANH · IDEAM · Gov.co)
🔄 ETL & Data Wrangling en Microsoft Fabric + Dataflows
🗂 Modelado dimensional (Hechos + Dimensiones + Jerarquías)
🧮 Cálculo de indicadores claves con DAX
📊 Visualización analítica avanzada en Power BI con navegación temática
Modelo construido bajo esquema estrella:
Tabla	Tipo	Descripción
Hechos_Producción	Fact	Producción, poder calorífico, operador, campo
Hechos_Regalías	Fact	Valor liquidado, TRM, volumen gravable
Hechos_Demanda	Fact	Series históricas + pronósticos por nodo
Dim_Fecha	Dimensión Calendario	Jerarquías Año–Mes–Día
Dim_Campo	Dimensión Sector Gasífero	Campos, operador, contrato
Dim_Region	Dimensión Geográfica	Departamento, municipio
Dim_Producción	Dimensión Técnica	Tipo producción, categoría

________________________________________

📁 Fuentes de Datos Usadas – con enlaces directos
Fuente	Tipo	Link
UPME – Datos energéticos nacionales	Producción / regalías	🔗 https://www.upme.gov.co/simec/planeacion-energetica/proyeccion_de_demanda/

ANH – Hidrocarburos Colombia	Campos · Regalías · Contratos	🔗 https://www.anh.gov.co

MinMinas	Comercio · Regalías · Políticas energéticas	🔗https://www.minenergia.gov.co/es/misional/hidrocarburos/funcionamiento-del-sector/gas-natural/

Gov.co – Open Data	Base cruda consolidada	🔗 https://www.datos.gov.co/Minas-y-Energ-a/Consolidaci-n-de-liquidaci-n-de-regal-as-por-campo/j7js-yk74/about_data 

Todos los datasets fueron ingeridos mediante Dataflows en Microsoft Fabric, transformados, limpiados, normalizados en un esquema tabular y posteriormente consumidos por Power BI.

________________________________________

📌 Dashboard – Navegación y Análisis
1. Producción de Gas Natural Nacional
📍 Visión macro del sistema productivo colombiano.
•	Evolución histórica & proyección futura
•	Operador con mayor participación
•	Producción por serie operativa (PP, PTDV, PC…)
•	Crecimiento compuesto estimado a 2034

________________________________________

2. Demanda de Gas Natural – Proyección y Análisis Territorial
📍 Escenarios de consumo & futuro energético nacional.
•	Series temporales histórico vs pronóstico
•	Escenarios proyectados 2024–2040
•	Principales nodos de consumo
•	Mapa térmico geográfico de demanda

________________________________________

3. Regalías – Evolución & Tendencias
📍 Liquidez, TRM y volatilidad anual.
•	Comportamiento de las regalías vs TRM
•	Distribución por tipo de producción
•	Campos principales contribuyentes
•	Sensibilidad del precio del gas

________________________________________

4. Regalías – Flujo Territorial y Volumetría
📍 Cómo se distribuye el dinero en el territorio.
•	Mapa geográfico por departamento
•	Volumen gravable en el tiempo
•	Segmentación por municipio + operador
________________________________________

5. Regalías – Detalle Operacional
📍 La vista granular para investigación profunda.
•	Tabla matriz filtrable por municipio & operador
•	Columnas con producción gravable y valor
•	Auditoría completa del sistema de regalías

________________________________________

🚀 Características Destacadas
✔ Análisis integral: producción - demanda - regalías
✔ Filtros aplicados a nivel nacional/territorial
✔ Modelo escalable con DAX avanzado
✔ Narrativa automática generada dinámicamente
✔ Proyección de escenarios energéticos futuros

________________________________________

🧬 Futuras Mejoras
Mejora	Posibilidad
Forecast más profundo ML + Azure AutoML	🔥
Segmentación de riesgo por reservas probadas	⚠
Detección de anomalías en producción	🤖
API en vivo para actualización continua	🌐

________________________________________

👥 Equipo de Desarrollo
Nombre	Rol
Brandon Parra	Data Analyst – BI Engineer
Ángel Parra	Data Analyst – BI Engineer
Anna Osorio	Modelado & documentación
Sebastián Moncada	Soporte y QA

🔗 GitHub:
https://github.com/bparra94/Observatorio-Integrado-del-Gas-Natural-Colombia-OIGN

📫 Contacto:
brandon17parra@hotmail.com

