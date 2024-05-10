# Ficha Técnica de la Base de Datos

## Características de los Datos

La base de datos contiene información sobre la estimación de población extranjera segmentada por comunas en Chile. Los datos provienen de fuentes oficiales y están actualizados hasta el año 2022.

Según INE: "Entregan una estimación acerca de la cantidad de personas extranjeras residentes habituales en Chile al 31 de diciembre de 2022 a nivel nacional, regional y para las comunas (con 10.000 o más personas extranjeras) de dicha estimación. 


## Alcance Metodológico

Los datos fueron recopilados y procesados por el Instituto Nacional de Estadísticas (INE) de Chile. La estimación de la población extranjera se realiza utilizando métodos estadísticos basados en datos de censos y encuestas poblacionales.

Este se hizo en conjunto con el Servicio Nacional de Migraciones (Sermig), Policía de Investigaciones (PDI), Ministerio de Relaciones 
Exteriores (Minrel) y el Servicio de Registro Civil e Identificación (SRCel). 

Según los datos que otorga INE sobre el estudio, desde el año 2018 se ha planteado un modelo de estimación de personas extranjeras que mantenga como bnase la agregación de datos provenientes del Censo 2017 y registros administrativos postcensales. 

El modelo se contempla de la siguiente manera: 

- Personas nacidas en el extranjero residentes habituales Censo 2017. 
- Sumado a personas en Registros Administrativos que permanecen en Chile (desde 2017 a 2022)
- Dando el total de estimación de personas extranjeras residentes habituales en Chile. 

En cuanto a la irregularidad de los extranjeros, se utilizan datos provenientes de PDI y de Sermig, sin embargo, se aclara que esta población no es 100% identificables. 

## Variables Incorporadas

| Variable        | Descripción                                                   |
|-----------------|---------------------------------------------------------------|
| SEXO            | Género de la población extranjera (H: Hombre, M: Mujer).      |
| EDAD            | Grupo de edad de la población extranjera.                     |
| PAIS            | País de origen de la población extranjera.                    |
| AÑO ESTIMACION  | Año de la estimación poblacional.                             |
| REGION          | Región geográfica de Chile donde se encuentra la comuna.      |
| COMUNA          | Nombre de la comuna en Chile.                                 |
| CENSO AJUSTADO  | Estimación de población extranjera ajustada según el censo.   |
| RRAA_REGULAR    | Estimación de población extranjera con residencia regular.    |
| RRAA_IRREGULAR  | Estimación de población extranjera con residencia irregular.  |
| RRAA_TOTAL      | Estimación total de población extranjera en la comuna.        |
| ESTIMACION      | Estimación total de población extranjera.                     |

## Observaciones

- Algunas variables tienen valores nulos debido a la falta de información en ciertas áreas geográficas o años.
- Las estimaciones de población extranjera pueden variar dependiendo de la precisión de los métodos utilizados y la disponibilidad de datos.
- Es importante tener en cuenta que estas estimaciones son solo aproximaciones y pueden no reflejar con precisión la población extranjera real en cada comuna, sobretodo en cuanto a población extranjera, puesto que INE reconoce estos datos como "no identificables". 
- Al revisar la tabla con los datos ya limpios, se percibe que la edad no está bien detallada. 
