Proyecto Final del curso de Análisis de datos - Equipo GROUP BY (6)
Título: Inclusión Educativa en Colombia: Análisis de la Capacidad Institucional para Atender a Estudiantes con Discapacidad en Contextos Rurales y Urbanos.

Descripción del reto: Proyecto de análisis exploratorio cuyo propósito es aplicar todas las etapas del análisis de datos, desde la limpieza hasta la visualización de resultados, la aplicación de metodologías ágiles, trabajo colaborativo y aplicación de modelos de aprendizaje automático supervisado.

Hipótesis a demostrar: “Las instituciones educativas en zonas urbanas están mejor preparadas para atender a estudiantes con discapacidad que las rurales.”

Hipótesis Nula (H₀): No hay diferencia significativa en la preparación para atender a estudiantes con discapacidad entre instituciones educativas urbanas y rurales.

Hipótesis Alternativa (H₁): “Existe una diferencia significativa en la preparación para atender a estudiantes con discapacidad entre instituciones urbanas y rurales.”

Método de organización: Para el desarrollo de este proyecto, aplicamos la metodología Daily Scrum, la cual nos permitió tener reuniones breves y constantes con el fin de revisar avances, identificar obstáculos y planificar tareas del día a día. Esta dinámica nos ayudó a mantener una comunicación fluida y a garantizar que todas las integrantes del equipo estuvieran alineadas con los objetivos del trabajo. Adicionalmente, utilizamos la herramienta Trello como tablero de gestión de tareas, en donde organizamos y distribuimos las actividades del proyecto en diferentes etapas: por hacer, en proceso y finalizado. Esta estructura nos permitió llevar un control visual del progreso individual y grupal, facilitando la colaboración y el cumplimiento de plazos.

Roles:

Líder del proyecto y coordinadora: Dayana Vasquez
Responsable de Limpieza y Preparación de Datos: Dayana Vasquez y Natasha Charris
Encargadas de la exploración y Análisis Descriptivo (EDA): Dayana Vasquez, Natasha Charris y Maria Fernanda Escobar.
Responsable del Modelado y aprendizaje automático (Machine Learning): Daniela Vergel
Encargada de la visualización y Dashboard: Michell Reinoso y Alejandra Donado
Encargadas de la documentación, diseño visual e identidad: Maria Fernanda Escobar, Alejandra Donado y Daniela Vergel.
Gestora del repositorio remoto y organización: Daniela Vergel.
Representante del grupo para la presentación final: Natasha Charris.
Pasos realizados:

Definición de hipótesis y enfoque de nuestro análisis: Se llegó a un acuerdo grupal para definir la hipótesis general que daría enfoque a nuestro proyecto, así como la pregunta de investigación, hipótesis nula e hipótesis alternativa. Esta parte del proceso se realizó luego de un analisis superficial de los datos contenidos en la base de datos propuesta por el equipo organizador del reto “Datathon”.

Extracción de datos: La base de datos propuesta por el equipo organizador fue descargada de la plataforma oficial del gobierno de la república de Colombia, Datos abiertos. Para este reto la base de datos se descargó en formato archivo CSV y se hizo la conversión a archivo excel para su posterior revisión.

Transformación y limpieza de datos: La primera parte de la transformación de datos se hizo en excel, el primer paso fue cambiar y dividir las columnas delimitadas por comas, para luego cambiar los caracteres especiales por sus respectivas letras.

Una vez limpio el archivo CSV, se hizo la conversión a archivo tipo excel. Se dividió la información en distintas hojas con la finalidad de transformar los datos categóricos más relevantes para nuestro análisis en una representación numérica binaria (0 o 1), lo que conocemos como One-Hot encoding.

Posteriormente a esta limpieza y transformación de datos, dimos inicio al proceso de limpieza profunda en Python, empleando principalmente la librería Pandas. Se utilizó principalmente la herramienta Google Colab. Las tres hojas principales del archivo Excel fueron leídas de forma independiente y luego combinadas mediante una unión horizontal (concatenación por columnas), dando lugar a un único DataFrame denominado df_unido.

A continuación, se procedió con la eliminación de duplicados, la revisión y tratamiento de valores nulos, y unificación de estructuras para asegurarnos de que los datos estuvieran en el formato correcto antes de aplicar técnicas de análisis más avanzadas. Este proceso permitió dejar el dataset en un estado consistente, sin duplicados, con valores nulos controlados, y con una estructura adecuada.

Proceso EDA: Durante el Análisis Exploratorio de Datos (EDA), se llevaron a cabo una serie de pasos enfocados en comprender la estructura, distribución y relaciones clave dentro del dataset. Se hizo la exploración general del dataset, el análisis de valores faltantes, un análisis más completo con la distribución de variables de interés, la revisión de correlaciones entre variables numéricas y la exploración de estrato socioeconómico y zona.

Durante el proceso se empleó el uso de visualizaciones mediante las librerías Seaborn y Matplotlib principalmente. Este análisis permitió tener una comprensión profunda de los datos disponibles, identificar patrones relevantes, y preparar el terreno para la selección de características y la aplicación de modelos de aprendizaje automático.

Carga de la información: Transferencia de los datos ya extraídos y transformados. Se extrae la base de datos final en formato de hoja de cálculo.

Aplicación de modelos de aprendizaje automático: Durante este proceso se aplicaron diversos modelos tanto de aprendizaje automático supervisado como no supervisado, en total se trabajaron con 5 modelos diferentes, pero solo 3 dieron resultados aceptables.

Dentro del código solo presentamos 3 modelos, dos de aprendizaje automático supervisado: Modelo de clasificación binaria y modelo de clasificación multiclase respectivamente, ambos emplearon un algoritmo random forest y otras utilidades de la biblioteca de aprendizaje automático Scikit-learn (sklearn).

Para el modelo de aprendizaje no supervisado se empleó un modelo de agrupación (Clustering), también utilizando la biblioteca Sickit-learn, el algoritmo de agrupamiento K-means y otras múltiples herramientas de la biblioteca, como el algoritmo RandomForestRegressor.

Visualizaciones y dashboard: Para la creación de l dashboard, se utilizó el dataset en archivo excel, el cual fue el resultado del proceso de limpieza y EDA. Posteriormente, se emplearon herramientas de visualización de datos para organizar y representar la información según zona geográfica, tipo de discapacidad, tipo de establecimiento, departamento y estrato socioeconómico. El resultado fue un tablero interactivo que permite filtrar y explorar los datos de manera dinámica, facilitando la identificación de patrones y brechas en la capacidad institucional para la inclusión educativa en contextos rurales, urbanos y mixtos.

Hallazgos: Para los hallazgos finales presentamos un análisis de la capacidad institucional para atender a estudiantes con discapacidad en contextos rurales, urbanos y mixtos en Colombia. A partir de los datos recopilados, se identificaron 10,254 establecimientos que atienden a estudiantes con discapacidad, distribuidos dentro de un total de 22,530 instituciones educativas. La mayoría de los casos se concentran en zonas urbanas (70.96%), seguidas por zonas rurales (18.6%) y mixtas (10.44%).

Las instituciones educativas urbanas son los principales centros que prestan atención a esta población. Entre los tipos de discapacidad más frecuentes se encuentran la discapacidad cognitiva, múltiple, síndrome de Down y lesión neuromuscular, con una mayor diversidad en zonas rurales. Los departamentos con mayor número de casos son Valle del Cauca, Bogotá D.C. y Córdoba, destacándose el primero por su alta concentración en zonas urbanas. Además, se observa que la mayoría de estudiantes con discapacidad pertenecen a estratos socioeconómicos 1 y 2, lo que indica una alta vulnerabilidad. Finalmente, el mapa incluido permite visualizar geográficamente los departamentos con mayor cobertura en inclusión educativa.

Pasos extra: Durante el proyecto se realizaron una serie de pasos extras enfocados en la documentación de los pasos realizados, hallazgos y creación del diseño e identidad de marca para nuestro proyecto, así como también la gestión y organización de archivos en el repositorio, tanto locales como en el remoto. Todas las integrantes participamos de esta parte del proceso en conjunto.

Links:

Link Trello: https://trello.com/invite/b/683f9d76d3d79e344cc4627b/ATTIa635e6f658f43ace38139596f51ae9ca1D9F7182/group-by-6-datathon

Link acceso dashboard (Power BI): https://app.powerbi.com/view?r=eyJrIjoiNDQwNTY4MzQtNDEyNS00YTg0LWIyMWUtYzYwNjZiMzkwNjE3IiwidCI6IjZjYTM0YWUxLTQ2NmYtNDRiYy1hN2FhLTBhYzVhNzhjNjFiMSIsImMiOjR9

Link de origen del Dataset empleado (ultima actualización: Febrero 2025): https://www.datos.gov.co/en/Educaci-n/ESTABLECIMIENTOS-EDUCATIVOS-COLOMBIA/upkm-vdjb/about_data

Archivo excel final para ejecutar el código: DATASET_LIMPIO_DATATHON_1.0 - DISCAPACIDADES DEPURADAS_v1 (lo encuentras en este repositorio)

Link presentación: https://www.canva.com/design/DAGqLDvgsjc/1iPqiTIkKrkVtH7MU4yjDA/view?utm_content=DAGqLDvgsjc&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=ha7365bac33
