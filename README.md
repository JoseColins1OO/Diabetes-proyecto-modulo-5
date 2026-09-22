## Parámetros de Carga (`fetch_ucirepo`)

Proporciona un ID de conjunto de datos o un nombre como argumentos de palabras clave (nombrados). No se pueden aceptar ambos a la vez.

* **`id`**: ID del conjunto de datos para el Repositorio UCI ML.
* **`name`**: Nombre del conjunto de datos, o subcadena del nombre.

---

## Estructura del Objeto Retornado (`dataset`)

* **`data`**: Contiene las matrices del conjunto de datos como dataframes de Pandas.
  * **`ids`**: Dataframe de columnas de identificación.
  * **`features`**: Dataframe de columnas de características (variables independientes).
  * **`targets`**: Dataframe de columnas objetivo (etiquetas).
  * **`original`**: Dataframe que consiste en todos los IDs, características y objetivos combinados.
* **`headers`**: Lista con todos los nombres/cabeceras de las variables.
* **`metadata`**: Contiene información de metadatos sobre el conjunto de datos (ver sección de Metadatos más abajo).
* **`variables`**: Contiene detalles de las variables presentados en un formato tabular/dataframe.
  * **`name`**: Nombre de la variable.
  * **`role`**: Si la variable es un ID, característica (`feature`) u objetivo (`target`).
  * **`type`**: Tipo de dato (ej. categórico, entero, continuo).
  * **`demographic`**: Indica si la variable representa datos demográficos.
  * **`description`**: Breve descripción de la variable.
  * **`units`**: Unidades de la variable para datos no categóricos.
  * **`missing_values`**: Si hay valores faltantes en la columna de la variable.

---

## Función `list_available_datasets`

Imprime una lista de conjuntos de datos que se pueden importar mediante `fetch_ucirepo`.

### Parámetros
* **`filter`**: Argumento opcional de palabra clave para filtrar los conjuntos de datos disponibles basado en una categoría. *Filtros válidos:* `aim-ahead`.
* **`search`**: Argumento opcional de palabra clave para buscar conjuntos de datos cuyo nombre contenga la consulta de búsqueda.
* **Retorno**: `none` (ninguno).

---

## Metadatos del Dataset (`metadata`)

* **`uci_id`**: Identificador único del conjunto de datos para el repositorio UCI.
* **`name`**: Nombre del dataset.
* **`abstract`**: Breve descripción del conjunto de datos.
* **`area`**: Área temática (ej. ciencias de la vida, negocios).
* **`task`**: Tareas asociadas de aprendizaje automático (ej. clasificación, regresión).
* **`characteristics`**: Tipos de conjuntos de datos (ej. multivariado, secuencial).
* **`num_instances`**: Número de filas o muestras.
* **`num_features`**: Número de columnas de características.
* **`feature_types`**: Tipos de datos de las características.
* **`target_col`**: Nombre de la(s) columna(s) objetivo.
* **`index_col`**: Nombre de la(s) columna(s) de índice.
* **`has_missing_values`**: Si el conjunto de datos contiene valores faltantes.
* **`missing_values_symbol`**: Indica qué símbolo representa las entradas faltantes (si el dataset tiene valores faltantes).
* **`year_of_dataset_creation`**: Año de creación del dataset.
* **`dataset_doi`**: DOI registrado para el conjunto de datos que enlaza a la página del repositorio UCI.
* **`creators`**: Lista de nombres de los creadores del dataset.
* **`intro_paper`**: Información sobre el artículo introductorio publicado del dataset.
* **`repository_url`**: Enlace a la página web del conjunto de datos en el repositorio UCI.
* **`data_url`**: Enlace al archivo de datos sin procesar (*raw data*).
* **`additional_info`**: Texto descriptivo libre sobre el dataset.
  * **`summary`**: Resumen general.
  * **`purpose`**: ¿Con qué propósito se creó el conjunto de datos?
  * **`funding`**: ¿Quién financió la creación del conjunto de datos?
  * **`instances_represent`**: ¿Qué representan las instancias en este conjunto de datos?
  * **`recommended_data_splits`**: ¿Existen divisiones de datos recomendadas?
  * **`sensitive_data`**: ¿Contiene el conjunto de datos información que pueda considerarse sensible de alguna manera?
  * **`preprocessing_description`**: ¿Se realizó algún preprocesamiento de datos?
  * **`variable_info`**: Descripción de texto libre adicional para las variables.
* **`citation`**: Solicitudes de citación / Agradecimientos.
* **`external_url`**: URL a la página externa del conjunto de datos. Este campo solo existirá para conjuntos de datos enlazados, es decir, no alojados por UCI.







# Estructura DATASET
| Variable Name | Role | Type | Demographic | Description | Units | Missing Values |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ID** | ID | Integer | no | Patient ID | no | no |
| **Diabetes_binary** | Target | Binary | no | 0 = no diabetes, 1 = prediabetes or diabetes | no | no |
| **HighBP** | Feature | Binary | no | 0 = no high BP, 1 = high BP | no | no |
| **HighChol** | Feature | Binary | no | 0 = no high cholesterol, 1 = high cholesterol | no | no |
| **CholCheck** | Feature | Binary | no | 0 = no cholesterol check in 5 years, 1 = yes cholesterol check in 5 years | no | no |
| **BMI** | Feature | Integer | no | Body Mass Index | no | no |
| **Smoker** | Feature | Binary | no | Have you smoked at least 100 cigarettes in your entire life? (0 = no, 1 = yes) | no | no |
| **Stroke** | Feature | Binary | no | (Ever told) you had a stroke. (0 = no, 1 = yes) | no | no |
| **HeartDiseaseorAttack** | Feature | Binary | no | Coronary heart disease (CHD) or myocardial infarction (MI). (0 = no, 1 = yes) | no | no |
| **PhysActivity** | Feature | Binary | no | Physical activity in past 30 days - not including job. (0 = no, 1 = yes) | no | no |
| **Fruits** | Feature | Binary | no | Consume fruit 1 or more times per day. (0 = no, 1 = yes) | no | no |
| **Veggies** | Feature | Binary | no | Consume vegetables 1 or more times per day. (0 = no, 1 = yes) | no | no |
| **HvyAlcoholConsump** | Feature | Binary | no | Heavy drinkers (adult men >14 drinks/wk, adult women >7 drinks/wk). (0 = no, 1 = yes) | no | no |
| **AnyHealthcare** | Feature | Binary | no | Have any kind of health care coverage, including health insurance, HMO, etc. (0 = no, 1 = yes) | no | no |
| **NoDocbcCost** | Feature | Binary | no | Past 12 months needed to see a doctor but couldn't because of cost. (0 = no, 1 = yes) | no | no |
| **GenHlth** | Feature | Integer | no | General health scale: 1 = excellent, 2 = very good, 3 = good, 4 = fair, 5 = poor | scale 1-5 | no |
| **MentHlth** | Feature | Integer | no | Days of poor mental health during the past 30 days (stress, depression, etc.) | scale 1-30 days | no |
| **PhysHlth** | Feature | Integer | no | Days of poor physical health during the past 30 days (illness/injury) | scale 1-30 days | no |
| **DiffWalk** | Feature | Binary | no | Do you have serious difficulty walking or climbing stairs? (0 = no, 1 = yes) | no | no |
| **Sex** | Feature | Binary | no | Sex: 0 = female, 1 = male | no | no |
| **Age** | Feature | Integer | no | Age 13-level category (1 = 18-24, ..., 13 = 80 or older) | scale 1-13 | no |
| **Education** | Feature | Integer | no | Education level scale (1 = Never attended school, ..., 6 = College graduate) | scale 1-6 | no |
| **Income** | Feature | Integer | no | Income scale (1 = less than $10,000, ..., 8 = $75,000 or more) | scale 1-8 | no |
