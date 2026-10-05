# Proyecto de Análisis de Datos: Patrones de Uso en ConnectaTel 📊

## 🎯 Objetivo del Proyecto
El objetivo principal de este proyecto es analizar el comportamiento real de uso de los clientes de ConnectaTel (empresa de telecomunicaciones) para identificar patrones de consumo en servicios móviles (llamadas y mensajes). A través del análisis de datos, se busca detectar diferencias significativas entre los usuarios del plan Básico y Premium, identificar valores atípicos (usuarios intensivos) y traducir estos hallazgos en recomendaciones estratégicas para la segmentación de clientes y optimización de la oferta comercial.

## 📂 Datasets Utilizados
El análisis se basa en dos conjuntos de datos principales:
* **`users`**: Contiene la información demográfica y de cuenta de los clientes. Incluye variables como `user_id`, `age`, `city`, `plan` (Básico/Premium), fecha de registro (`reg_date`) y fecha de abandono (`churn_date`).
* **`usage`**: Contiene el registro detallado de las actividades de los usuarios. Incluye variables como `user_id`, fecha de la acción (`date`), tipo de acción (`type`: llamada o mensaje), duración en minutos (`duration`) y longitud (`length`).

## 🛠️ Etapas del Análisis Realizadas
1. **Exploración Inicial:** Carga de los datos y revisión preliminar de la estructura, tipos de datos y valores generales.
2. **Limpieza y Preprocesamiento de Datos:**
   * Corrección de tipos de datos (conversión de `user_id` a formato de texto).
   * Tratamiento de valores nulos (identificación de datos *Missing at Random* en duración de llamadas y mensajes).
   * Identificación y manejo de anomalías y valores "sentinel" (fechas futuras en registros, edad capturada como `-999` y ciudades registradas como `?`).
3. **Agrupación y Fusión de Datos:** Creación de un perfil unificado por usuario (`user_profile`) calculando métricas de uso total (cantidad de mensajes, cantidad de llamadas y minutos consumidos) mediante la integración (`merge`) de los datasets.
4. **Análisis Exploratorio de Datos (EDA):** Visualización de datos mediante histogramas y diagramas de caja (boxplots) para entender la distribución, la asimetría y el rango intercuartílico de variables clave como edad y niveles de uso.
5. **Generación de Insights y Análisis Ejecutivo:** Extracción de conclusiones de negocio, evaluación del impacto de los valores atípicos (outliers) reales y formulación de recomendaciones accionables.

## 🚀 Cómo ejecutar el notebook
Puedes visualizar e interactuar con este proyecto de dos formas:

**Opción A: Usando Google Colab (Recomendado)**
1. Sube el archivo `.ipynb` a tu cuenta de Google Drive.
2. Haz clic derecho sobre el archivo > Abrir con > Google Colaboratory.
3. Asegúrate de cargar los archivos CSV correspondientes en el entorno de ejecución de Colab o ajustar las rutas de lectura en el código.

**Opción B: Entorno Local (Jupyter Notebook)**
1. Asegúrate de tener instalado Python y Jupyter Notebook (o JupyterLab).
2. Clona este repositorio en tu máquina local.
3. Abre una terminal en la carpeta del repositorio y ejecuta el comando: `jupyter notebook`.
4. Abre el archivo principal del proyecto.

## 📋 Breve guía de reproducción
Para reproducir exactamente los mismos resultados de este análisis, sigue estos pasos:
1. **Clonar el repositorio:** 
   ```bash
   git clone <URL_DEL_REPOSITORIO>
