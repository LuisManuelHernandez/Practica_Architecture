## 🌐 Big Data Architecture: Integración Hadoop & ElasticSearch

Este repositorio contiene la solución técnica a la práctica avanzada de Arquitectura de Big Data. El proyecto se centra en la interoperabilidad entre ecosistemas de procesamiento masivo (Hadoop/Hive) y motores de búsqueda y analítica en tiempo real (ElasticSearch/Kibana).

🎯 Objetivos del Proyecto
- Configurar un entorno de Big Data en Google Cloud Platform (GCP).
- Establecer una conexión funcional entre Apache Hive y un índice de ElasticSearch.
- Realizar ingesta, transformación y consulta de datos cruzados entre ambas plataformas.
- Visualizar los resultados mediante dashboards dinámicos.

🛠️ Stack Tecnológico
- Infraestructura: Google Cloud Platform (Compute Engine / Dataproc).
- Almacenamiento y Procesamiento: Hadoop HDFS y Apache Hive.
- Motor de Búsqueda: ElasticSearch.
- Visualización: Kibana.
- Conector: elasticsearch-hadoop (JAR).

📂 Estructura del Repositorio
- PRÁCTICA_ElasticSearch_Hadoop.ipynb: Guía detallada con las instrucciones, conceptos teóricos y pasos necesarios para la integración de los sistemas.
- PRACTICA RESUELTA BIG DATA ARCHITECTURE.pdf: Informe final que documenta la ejecución exitosa, capturas de pantalla de la consola de GCP, consultas en Hive y la creación del índice en ElasticSearch.

📝 Fases de la Práctica

1. Configuración del Entorno en GCP
Despliegue de instancias en Google Cloud y configuración de reglas de firewall para permitir la comunicación en los puertos de ElasticSearch (9200) y Kibana (5601).

2. Conector Hadoop-ElasticSearch
Instalación del conector .jar necesario para que Hive pueda "hablar" con ElasticSearch, permitiendo que una tabla externa de Hive vuelque o consulte datos directamente en un índice.

3. Modelado en Hive
Creación de tablas externas vinculadas mediante org.elasticsearch.hadoop.hive.EsStorageHandler.

4. Consultas y Verificación
Ejecución de comandos CURL para verificar la existencia de los documentos en el clúster de ElasticSearch y validación de la consistencia de los datos.

5. Visualización en Kibana
Exploración de la herramienta Analytics > Dashboards para crear visualizaciones sobre los datos indexados, permitiendo un análisis visual inmediato.

🚀 Cómo replicar
- Sigue los pasos de configuración de red en GCP detallados en el PDF.
- Asegúrate de que los servicios de Hadoop y ElasticSearch estén activos.
- Carga el conector en la sesión de Hive: ADD JAR path/to/elasticsearch-hadoop-X.X.X.jar;
- Ejecuta las sentencias DDL proporcionadas para crear la conexión.
