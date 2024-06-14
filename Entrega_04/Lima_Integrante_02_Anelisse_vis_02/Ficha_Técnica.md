### Ficha Técnica - Venezuela vs otras nacionalidades

#### Descripción 

Este documento describe la codificación de las dimensiones y variables utilizadas en la base de datos de la distribución regional de las personas de Venezuela en Chile versus otras nacionalidades. La información fue obtenida de la [Minuta de población migrante de Venezuela en Chile](https://serviciomigraciones.cl/wp-content/uploads/estudios/Minutas-Pais/Venezuela.pdf) que contiene datos estadísticos de la población migrante de Venezuela en Chile. Esta base de datos se hizo manualmente a través de los documentos emitidos por el Servicio Nacional de Migraciones, SERMIG.  

#### Variables Incorporadas

| Variable     | Descripción                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------|
| `Región`       | Indica la región de destino en la residen los migrantes venezolanos. Esta columna contiene los nombres de las regiones.       |
| `Tarapacá`   | Porcentaje de migrantes venezolanos que residen en la región de Tarapacá.            |
| `Arica y Parinacota` | Porcentaje de migrantes venezolanos que residen en la región de Arica y Parinacota. |
| `Antofagasta`| Porcentaje de migrantes venezolanos que residen en la región de Antofagasta.         |
| `Atacama`    | Porcentaje de migrantes venezolanos que residen en la región de Atacama.             |
| `Coquimbo`   | Porcentaje de migrantes venezolanos que residen en la región de Coquimbo.            |
| `Valparaíso` | Porcentaje de migrantes venezolanos que residen en la región de Valparaíso.          |
| `Metropolitana` | Porcentaje de migrantes venezolanos que residen en la región Metropolitana.       |
| `O'Higgins`  | Porcentaje de migrantes venezolanos que residen en la región de O'Higgins.           |
| `Maule`      | Porcentaje de migrantes venezolanos que residen en la región del Maule.              |
| `Ñuble`      | Porcentaje de migrantes venezolanos que residen en la región de Ñuble.               |
| `Biobío`     | Porcentaje de migrantes venezolanos que residen en la región del Biobío.             |
| `La Araucanía` | Porcentaje de migrantes venezolanos que residen en la región de La Araucanía.      |
| `Los Ríos`   | Porcentaje de migrantes venezolanos que residen en la región de Los Ríos.            |
| `Los Lagos`  | Porcentaje de migrantes venezolanos que residen en la región de Los Lagos.           |
| `Aysén`      | Porcentaje de migrantes venezolanos que residen en la región de Aysén.               |
| `Magallanes y La Antártica` | Porcentaje de migrantes venezolanos que residen en la región de Magallanes y La Antártica. |

#### Representación de las Variables

- **otras nacionalidades**: Esta variable categórica indica el porcentaje de todas las nacionalidades existentes de migrantes por región excepto la venezolana
- **Venezuela**: Esta variable categórica indica el porcentaje de población migrante venezolana de acuerdo a cada región.
- **Regiones**: Corresponde a una región de Chile y contiene datos porcentuales que indican el porcentaje de migrantes venezolanos en comparación a las otras nacionalidades.

#### Notas Adicionales

- Los porcentajes se indican en formato decimal (por ejemplo, 12.34% se representa como 12,34 en la base de datos).
- El análisis se realizó para identificar la nacionalidad con mayor porcentaje de migrantes en cada región, en este caso Venezuela a comparación de todas las otras nacionalidades. 
  


### Ficha Técnica - Países con mayor volumen de inmigración venezolana 

#### Descripción 

Describe la codificación de las dimensiones y variables utilizadas en la base de datos de países con mayor volumen de inmigración venezolana. La información fue obtenida de la [Coordinación interagencial para refugiados y migrantes de Venezuela](https://www.r4v.info/es/refugiadosymigrantes) así como el [STATISTA](https://es.statista.com/estadisticas/1261404/paises-con-mayor-numero-de-migrantes-venezolanos-en-el-mundo/) que contienen datos estadísticos de la población migrante de Venezuela en al rededor del mundo. Esta base de datos se hizo manualmente a través de dichos datos.

#### Variables Incorporadas

| Variable     | Descripción                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------|
| `País`       | Indica el país de destino los migrantes venezolanos. Esta columna contiene los nombres de los países.       |
| `Número de venezolanos por país`   | Cantidad de migrantes venezolanos que residen en cada país latinoamericano.            |

#### Notas Adicionales

- El análisis se realizó para identificar el país con mayor porcentaje de migrantes venezolanos. 
  
