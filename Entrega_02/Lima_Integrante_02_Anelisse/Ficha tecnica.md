# FICHA TÉCNICA DE LA BASE DE DATOS - REGIONES

## Características de los Datos

La base de datos contiene información sobre la estimación de población extranjera segmentada por comunas en Chile. Los datos provienen de fuentes oficiales y están actualizados hasta el año 2022.

Según INE: "Entregan una estimación acerca de la cantidad de personas extranjeras residentes habituales en Chile al 31 de diciembre de 2022 a nivel nacional, regional y para las comunas (con 10.000 o más personas extranjeras) de dicha estimación. 


## Alcance Metodológico

Los datos fueron recopilados y procesados por el Instituto Nacional de Estadísticas (INE) de Chile. La estimación de la población extranjera se realiza utilizando métodos estadísticos basados en datos de censos y encuestas poblacionales.

Este se hizo en conjunto con el Servicio Nacional de Migraciones (Sermig), Policía de Investigaciones (PDI), Ministerio de Relaciones 
Exteriores (Minrel) y el Servicio de Registro Civil e Identificación (SRCel). 

Según los datos que otorga INE sobre el estudio, desde el año 2018 se ha planteado un modelo de estimación de personas extranjeras que mantenga como base la agregación de datos provenientes del Censo 2017 y registros administrativos postcensales. 

El modelo se contempla de la siguiente manera: 

- Personas nacidas en el extranjero residentes habituales Censo 2017. 
- Sumado a personas en Registros Administrativos que permanecen en Chile (desde 2017 a 2022)
- Dando el total de estimación de personas extranjeras residentes habituales en Chile. 

En cuanto a la irregularidad de los extranjeros, se utilizan datos provenientes de PDI y de Sermig, y se especifíca que esta no población no es del todo identificable.

## Variables Incorporadas

| Variable        | Descripción                                                   |
|-----------------|---------------------------------------------------------------|
| SEXO            | Género de la población extranjera (H: Hombre, M: Mujer).      |
| EDAD            | Grupo de edad de la población extranjera.                     |
| PAIS            | País de origen de la población extranjera.                    |
| AÑO ESTIMACION  | Año de la estimación poblacional.                             |
| REGION          | Región geográfica de Chile donde se encuentra la comuna.      |
| CÓDIGO REGIÓN   | Código de la región demográfica en Chile                      |
| CENSO AJUSTADO  | Estimación de población extranjera ajustada según el censo.   |
| RRAA_REGULAR    | Estimación de población extranjera con residencia regular.    |
| RRAA_IRREGULAR  | Estimación de población extranjera con residencia irregular.  |
| RRAA_TOTAL      | Estimación total de población extranjera en la comuna.        |
| ESTIMACION      | Estimación total de población extranjera.                     |

## Observaciones

- Hay una cantidad considerable de valores nulos en cada variable debido a falta de información.
- La base regional tiene 11 variables y 51.946 registros, mientras que la base comunal tiene 11 variables y 123.986
registros. Las variables de la base de región son: sexo, edad, país, año, estimación, codigo region, region, censo ajustado, rraa regular, rraa irregular, rraa total, estimación. 
- Es importante tener en cuenta que estas estimaciones son solo aproximaciones y pueden no reflejar con precisión la población extranjera real en cada comuna, sobretodo en cuanto a población extranjera, puesto que INE reconoce estos datos como "no identificables". 
- Se resalta que se ocuparon las bases de datos enviadas por el Servicio de Registro Civil e Identificación con la información de las personas migrantes fallecidas desde 2015 al 31 de diciembre de 2022. 
- No se especifican las edades, más bien se utiliza un rango de ellas. 