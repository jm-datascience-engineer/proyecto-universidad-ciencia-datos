# Dashboard: Bajo peso al nacer en hijos de madres adolescentes

Dashboard interactivo desarrollado como parte del Proyecto Aplicado de la Especialización en Ciencia de Datos y Analítica de la Universidad Nacional Abierta y a Distancia (UNAD).

## Descripción del proyecto

Este proyecto presenta una herramienta de visualización de datos orientada al análisis del bajo peso al nacer en hijos de madres adolescentes. El dashboard permite explorar características de los registros, observar patrones descriptivos y comunicar los resultados obtenidos durante el proceso de análisis y evaluación de modelos predictivos.

La solución utiliza tecnologías web para presentar los resultados en una interfaz interactiva, con una organización visual inspirada en los tableros de analítica de datos del sector salud.

## Objetivo general

Desarrollar un dashboard interactivo que facilite la exploración, visualización e interpretación de información relacionada con el bajo peso al nacer en hijos de madres adolescentes, como apoyo a la comunicación de resultados del Proyecto Aplicado.

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
- Interfaz construida con HTML, CSS y JavaScript.
- Visualización directamente desde un navegador web, sin necesidad de instalar un servidor.

## Tecnologías utilizadas

- **HTML5:** estructura de la interfaz.
- **CSS3:** estilos, distribución y diseño adaptable.
- **JavaScript:** generación de gráficos e interactividad.
- **Python y pandas:** herramientas utilizadas para el procesamiento de datos, cuando corresponda.
- **Jupyter Notebook:** entorno de trabajo para el análisis y desarrollo del proyecto.

## Fuente de datos

El análisis se basa en el archivo CSV utilizado durante el desarrollo del Proyecto Aplicado, que contiene inicialmente **9.513 registros y 51 variables**.

Antes de publicar o redistribuir los datos, es necesario verificar las condiciones de uso, confidencialidad y autorización correspondientes. Por esta razón, el conjunto de datos original no se incluye necesariamente en este repositorio.

## Estructura del repositorio

```text
dashboard-bajo-peso-nacer/
├── README.md
├── LICENSE
├── .gitignore
├── dashboard_plantilla_salud_materna.html
└── notebooks/
    └── analisis.ipynb
    └── modelos_adicionales.ipynb
```

## Cómo ejecutar el dashboard

No necesitas instalar dependencias para abrir la versión HTML estática.

1. Clona el repositorio o descarga sus archivos desde GitHub.
2. Localiza el archivo `dashboard_plantilla_salud_materna.html`.
3. Ábrelo con un navegador actualizado, como Google Chrome, Microsoft Edge o Firefox.
4. Explora las secciones disponibles y utiliza los controles interactivos.

Si deseas publicar el dashboard en línea, puedes evaluar GitHub Pages, siempre que los archivos y datos incluidos sean apropiados para su publicación pública.

## Consideraciones metodológicas

Los resultados dependen de la calidad de los datos, las transformaciones realizadas y la codificación de las variables.

En particular, la clasificación del bajo peso al nacer requiere verificar la unidad original de la variable de peso y la regla de conversión aplicada. Las categorías representadas mediante códigos deben contrastarse con el diccionario oficial de datos antes de interpretar sus significados.

Los indicadores y las métricas predictivas deben coincidir con los resultados definitivos del análisis. Si se actualiza el procesamiento o se vuelven a entrenar los modelos, es necesario revisar también las cifras presentadas en el dashboard.

## Evaluación de modelos predictivos

El proyecto contempla la comparación de modelos de clasificación, entre ellos:

- Regresión logística.
- Árbol de decisión.
- Random Forest.

La evaluación debe considerar métricas como ROC-AUC, PR-AUC, sensibilidad, especificidad y F1-score, de acuerdo con los resultados documentados en el análisis.

Dado que el problema puede presentar desbalance entre clases, la exactitud por sí sola no es suficiente para valorar el desempeño de los modelos. La selección del umbral de clasificación también debe responder al objetivo del análisis y al costo de los errores de predicción.

Las métricas presentadas deben verificarse contra el notebook final antes de utilizarlas como resultados definitivos.

## Limitaciones y uso responsable

Este dashboard tiene fines académicos y de comunicación de resultados. No constituye un sistema de diagnóstico clínico ni debe utilizarse por sí solo para tomar decisiones médicas individuales.

Los patrones observados representan asociaciones descriptivas y no demuestran relaciones causales. El desempeño obtenido durante la evaluación interna tampoco garantiza que los modelos funcionen de la misma manera en otras poblaciones o conjuntos de datos.

La interpretación debe considerar la calidad de los registros, los valores faltantes, el posible desbalance de clases y las limitaciones del proceso de modelado.

## Contexto académico

**Institución:** Universidad Nacional Abierta y a Distancia (UNAD)  
**Programa:** Especialización en Ciencia de Datos y Analítica  
**Curso:** Proyecto de Grado II  
**Estrategia metodológica:** Aprendizaje Basado en Proyectos (ABP)  
**Etapa:** Visualización y comunicación de resultados

**Autor:** Juan Meriño Mercado  
**Año:** 2026

Este repositorio corresponde a un desarrollo académico y no implica patrocinio, certificación ni aval institucional por parte de la UNAD o de entidades del sector salud.

## Licencia

Consulta el archivo `LICENSE` para conocer las condiciones de uso del código original incluido en este repositorio.

La licencia del código no concede automáticamente derechos de uso o redistribución sobre los datos, las marcas institucionales, las imágenes ni otros materiales de terceros.

## Uso ético de herramientas de inteligencia artificial

Las herramientas de inteligencia artificial pueden utilizarse como apoyo al desarrollo, la documentación y la revisión del proyecto. Su uso debe realizarse de forma transparente y responsable, verificando los resultados generados y manteniendo la responsabilidad académica sobre el contenido, el análisis y las conclusiones.

## Estado del proyecto

Dashboard académico en desarrollo y validación. Las transformaciones de los datos, las etiquetas categóricas y los indicadores finales deben verificarse antes de presentar los resultados como definitivos.
