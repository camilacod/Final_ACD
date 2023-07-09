# Título del Proyecto

# 1. Identificación del Problema

## Contexto 

Durante los años 2017 y 2018, se llevó a cabo la encuesta VIANEV (Vigilancia Alimentaria Nutricional por Etapas de Vida) en todo el territorio de Perú. Esta encuesta fue realizada tanto en zonas urbanas como rurales, específicamente en hogares con niños menores de 3 años.

## Naturaleza de los datos

Los datos fueron recopilados mediante encuestas en dos fases: 
- Primera fase: del 16 de octubre al 28 de diciembre de 2017.
- Segunda fase: del 26 de febrero al 13 de mayo de 2018.

Estas encuestas estuvieron a cargo de la Dirección Ejecutiva de Vigilancia Alimentaria y Nutricional - Centro Nacional de Alimentación y Nutrición – Instituto Nacional de Salud (CENAN - INS). El objetivo principal de esta encuesta era describir el estado nutricional de los niños menores de 3 años en Perú.

Las encuestas fueron conducidas por equipos compuestos por un supervisor de equipo, dos encuestadores nutricionistas, un encuestador bioquímico, cuatro profesionales para control de calidad, un jefe de campo, un apoyo administrativo y el equipo técnico de VIANEV compuesto por seis personas.

Tras la recolección de los datos, se digitalizaron y verificaron en la interfaz de CENAN. Se realizaron controles de calidad para garantizar la consistencia de los datos, como la verificación de las fechas de nacimiento y que los sujetos de estudio cumplieran con el rango de edad establecido (menores de 35 meses), entre otros aspectos.

Finalmente, los datos fueron publicados y están disponibles en: https://www.datosabiertos.gob.pe/dataset/encuesta-vianev-2017-2018-estado-nutricional-en-ni%C3%B1os-menores-de-3-a%C3%B1os-ins-cenan.

El archivo descargado en formato ZIP contiene la siguiente estructura:

- Bases: 12 archivos Excel representando la base de datos titulada "CAP"+ 3 dígitos.
- Factor: Base de datos que presenta datos generales de las encuestas VIANEV y códigos de diferenciación. No se dispone de un diccionario para esta base de datos.
- Diccionarios: 12 archivos Excel que proporcionan interpretaciones a las columnas de las relaciones en las bases de datos mencionadas anteriormente.

## Potencial e importancia del análisis a realizar

A diferencia de años anteriores, no se publicó un informe técnico con los resultados de la encuesta. Por tanto, surge la necesidad de realizar un análisis de los datos recolectados, con el objetivo de poner a disposición del público esta información. Si bien el objetivo original era describir el estado nutricional de los niños menores de 3 años, consideramos importante dar un enfoque adicional y concentrarse en los subgrupos de la población estudiada y en particular en la lucha contra la anemia, un problema de salud grave que afecta a un gran porcentaje de la población infantil en Perú.

## Potenciales usuarios

El análisis de estos datos será de interés para el INS, la comunidad científica y el público en general interesado en conocer las relaciones entre las condiciones sociales, geográficas, de género, educativas y culturales de los niños y su estado nutricional. Especialmente relevante es la relación entre estos factores y la incidencia de la anemia en esta población.

## 2. Data Pipeline

### Extract
Aquí debes incluir información sobre el conjunto de datos que estás utilizando. Por ejemplo, puedes incluir información como:
- Resumen del dataset: ¿De qué trata el dataset?
- Diccionario del dataset: ¿Qué representan cada una de las columnas en tu dataset?
- Tamaño del dataset: ¿Cuántas filas y columnas tiene tu dataset?

### Load
Presenta aquí el diagrama del pipeline identificando si es un ELT o un ETL. No olvides incluir el enlace a la base de datos en Postgres si está disponible.

### Transform
Explica aquí cada uno de los pasos de la transformación que realizaste, incluyendo las tareas de preprocesamiento y la eliminación de outliers. También puedes mencionar aquí si has creado un datamart y por qué.

## 3. Insights
Explica aquí qué insights interesantes has encontrado a través del análisis computacional de los datos.

## 4. Conclusiones
Realiza aquí un análisis global de tu proyecto. Piensa en lo que has aprendido, los desafíos que has enfrentado y las soluciones que has encontrado. También puedes reflexionar sobre lo que estos resultados podrían significar en el contexto más amplio del problema que estás tratando de resolver.

## Referencias
Si has utilizado fuentes externas para tu análisis, es importante citarlas aquí.
