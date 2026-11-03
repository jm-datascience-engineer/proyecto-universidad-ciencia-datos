# Dashboard: Bajo peso al nacer en hijos de madres adolescentes

Dashboard interactivo desarrollado como parte del Proyecto Aplicado de la Especialización en Ciencia de Datos y Analítica de la Universidad Nacional Abierta y a Distancia (UNAD).

**Ver el dashboard en línea:** [https://jm-datascience-engineer.github.io/proyecto-universidad-ciencia-datos/](https://jm-datascience-engineer.github.io/proyecto-universidad-ciencia-datos/)

## Descripción del proyecto

Este proyecto presenta una herramienta de visualización de datos orientada al análisis del bajo peso al nacer en hijos de madres adolescentes. El dashboard permite explorar las características de los registros, observar patrones descriptivos y comunicar los resultados del análisis y de la evaluación de modelos predictivos.

La solución utiliza tecnologías web para presentar los resultados en una interfaz interactiva, con una organización visual inspirada en los tableros de analítica de datos del sector salud.

## Objetivo general

Desarrollar un dashboard interactivo que facilite la exploración, visualización e interpretación de la información relacionada con el bajo peso al nacer en hijos de madres adolescentes, como apoyo a la comunicación de resultados del Proyecto Aplicado.

## Objetivos específicos

- Visualizar indicadores descriptivos de los registros analizados.
- Explorar la distribución de los datos según la edad materna y las consultas prenatales.
- Examinar patrones relacionados con la clasificación del peso al nacer.
- Presentar los resultados de la evaluación de modelos de clasificación.
- Comunicar los hallazgos y las limitaciones del análisis de manera clara y comprensible.

## Características principales

- Dashboard web con diseño adaptable a diferentes tamaños de pantalla.
- Indicadores generales del conjunto de datos.
- Gráficos descriptivos sobre edad materna, peso al nacer y consultas prenatales.
- Sección de análisis exploratorio.
- Sección de evaluación y comparación de modelos predictivos.
- Interfaz construida con HTML, CSS y JavaScript en un único archivo.
- Visualización directamente desde un navegador web, sin instalar dependencias ni configurar un servidor.

## Tecnologías utilizadas

- **HTML5, CSS3 y JavaScript:** estructura, estilos, gráficos e interactividad del dashboard.
- **Python:** procesamiento de datos y modelado, con las librerías pandas, NumPy, SciPy, scikit-learn, Matplotlib y Seaborn.
- **Jupyter Notebook:** entorno de trabajo para el análisis y desarrollo del proyecto.

## Fuente de datos

El análisis utiliza el conjunto de datos abierto **Embarazo en adolescentes**, publicado por la Dirección Territorial de Salud de Caldas en el portal de Datos Abiertos Colombia:
[https://www.datos.gov.co/Salud-y-Protecci-n-Social/Embarazo-en-adolescentes/dpcy-dq5j/about_data](https://www.datos.gov.co/Salud-y-Protecci-n-Social/Embarazo-en-adolescentes/dpcy-dq5j/about_data)

El archivo `Embarazo_en_adolescentes_20260908.csv`, incluido en este repositorio, corresponde a la descarga del 8 de septiembre de 2026 y contiene inicialmente **9.513 registros y 51 variables**. Su uso debe respetar las condiciones establecidas por el portal de origen.

## Estructura del repositorio

```text
proyecto-universidad-ciencia-datos/
├── README.md
├── LICENSE
├── .gitignore
├── Embarazo_en_adolescentes_20260908.csv
├── index.html
└── notebooks/
    ├── analisis.ipynb
    └── modelos_adicionales.ipynb
```

- **`index.html`:** dashboard interactivo.
- **`notebooks/analisis.ipynb`:** análisis completo por etapas: comprensión y preparación de los datos, análisis exploratorio, entrenamiento de los modelos y evaluación.
- **`notebooks/modelos_adicionales.ipynb`:** notebook complementario que, por recomendación del asesor, compara el modelo completo con dos configuraciones sin las variables de mayor peso: sin `T_GES`, `NUMCONSUL` y `SEXO`, y sin `T_GES` y `NUMCONSUL`.

Cada notebook incluye una portada y una descripción antes de cada bloque de código.

## Cómo ejecutar el dashboard

La versión HTML no requiere instalar dependencias.

1. Clone el repositorio o descargue sus archivos desde GitHub.
2. Localice el archivo `index.html`.
3. Ábralo con un navegador actualizado, como Google Chrome, Microsoft Edge o Firefox.
4. Explore las secciones disponibles y utilice los controles interactivos.

También puede consultarlo en línea en el enlace indicado al inicio de este documento.

## Cómo ejecutar los notebooks

Los notebooks pueden abrirse en Jupyter Notebook, JupyterLab, Visual Studio Code o Google Colab (**Archivo → Subir cuaderno**). Requieren Python 3 con las librerías indicadas en la sección de tecnologías y el archivo CSV del repositorio en la ruta que define el código.

## Consideraciones metodológicas

La variable objetivo `BAJO_PESO` se definió como un peso al nacer inferior a 2.500 gramos. Durante la preparación de los datos se identificó y trató el valor especial 9.999 en la variable de peso y se normalizó su unidad antes de construir la clasificación.

Las variables categóricas se analizaron a partir de los códigos del conjunto de datos de origen. Su interpretación debe apoyarse en el diccionario de datos publicado por la entidad responsable.

Los resultados dependen de la calidad de los registros, de las transformaciones realizadas y de la codificación de las variables.

## Evaluación de modelos predictivos

El proyecto compara los siguientes modelos de clasificación:

- Regresión logística.
- Árbol de decisión.
- Random Forest.

Los modelos se evaluaron con las métricas ROC-AUC, PR-AUC, sensibilidad, especificidad y F1-score. Los valores obtenidos se presentan en el dashboard y en el notebook `analisis.ipynb`.

Debido al desbalance entre clases, la exactitud por sí sola no es suficiente para valorar el desempeño de los modelos. Por esa razón, la selección del umbral de clasificación se orientó al objetivo del análisis y al costo de los errores de predicción.

El dashboard incluye además una sección que permite comparar el desempeño de los modelos al excluir el número de consultas prenatales, el tiempo de gestación y el sexo del recién nacido.

## Limitaciones y uso responsable

Este dashboard tiene fines académicos y de comunicación de resultados. No constituye un sistema de diagnóstico clínico ni debe utilizarse por sí solo para tomar decisiones médicas individuales.

Los patrones observados representan asociaciones descriptivas y no demuestran relaciones causales. El desempeño obtenido en la evaluación interna tampoco garantiza que los modelos funcionen de la misma manera en otras poblaciones o conjuntos de datos.

La interpretación debe considerar la calidad de los registros, los valores faltantes, el desbalance de clases y las limitaciones del proceso de modelado.

## Contexto académico

**Institución:** Universidad Nacional Abierta y a Distancia (UNAD)  
**Programa:** Especialización en Ciencia de Datos y Analítica  
**Curso:** Proyecto de Grado II (203008071A_2204)  
**Estrategia metodológica:** Aprendizaje Basado en Proyectos (ABP)  
**Etapa:** Visualización y comunicación de resultados

**Autor:** Juan Manuel Meriño Mercado  
**Asesor y director:** Rafael Gaitán Ospina  
**Año:** 2026

Este repositorio corresponde a un desarrollo académico y no implica patrocinio, certificación ni aval institucional por parte de la UNAD o de entidades del sector salud.

## Licencia

El código original de este repositorio se distribuye bajo la licencia MIT. Consulte el archivo `LICENSE` para conocer sus condiciones.

La licencia del código no se extiende a los datos, las marcas institucionales, las imágenes ni otros materiales de terceros, que conservan sus propias condiciones de uso.

## Uso de herramientas de inteligencia artificial

En el desarrollo del proyecto se utilizaron herramientas de inteligencia artificial como apoyo en la programación, la documentación y la revisión. El autor verificó los resultados generados y mantiene la responsabilidad académica sobre el contenido, el análisis y las conclusiones.

## Estado del proyecto

Versión de entrega correspondiente a la etapa de visualización y comunicación de resultados del Proyecto Aplicado.
