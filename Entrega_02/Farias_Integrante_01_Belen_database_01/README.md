## Belén Farías
###  Paso a paso:

- Busqué y descargué un arcvhivo csv desde la página del Instituto Nacional de Estadísticas. Esto debido a que es una fuente de caracter oficial y con datos actualizados. En este caso, encontré una relacionada a la estimación de población extranjera en 2022 segmentada por comunas. 

- Abrí Google Colab y cree un nuevo cuaderno. Intenté conectar mi Google Drive al cuaderno. Por algún motivo, me arrojó error. Descubrí que era porque la cuenta que estaba intentando vincular y la que estaba conectada al colab, eran distinas. 

- Una vez conectado el drive, mediante el codigo: 

from google.colab import drive
drive.mount('/content/drive')

Procedo con escribir: import panda as pd

al comienzo del código, pues esto me ayudará a importar la biblioteca de Pandas, para facilitar el uso de las funciones que usaremos en el cuaderno. 

- Experimenté problemas para importar la base de datos, pues ningún codigo me funcionaba. Solicité a Chat GPT que me dijera cuál era el problema específico y cómo solucionarlo, copiando y pegando el código de error que me arrojaba colab. Finalmente, resultó haber un problema en el formato de codificación de la tabla de origen, su explicación y resolución fue la siguiente: 


El error UnicodeDecodeError indica que Pandas está teniendo problemas para decodificar el archivo CSV utilizando el formato de codificación predeterminado (UTF-8). Esto podría suceder si el archivo CSV contiene caracteres que no son compatibles con UTF-8.

Para resolver este problema, puedes intentar especificar explícitamente la codificación al leer el archivo CSV. Aquí tienes cómo hacerlo:

code: 

python
Copy code
import pandas as pd

#Ruta al archivo CSV en tu Google Drive
file_path = '/content/drive/My Drive/GRAFICA/base-2022-comunas.csv'

#Especificar la codificación al leer el archivo CSV

df = pd.read_csv(file_path, encoding='latin1')

"En este caso, he utilizado encoding='latin1', que es otro formato de codificación comúnmente utilizado. Sin embargo, si esto no resuelve el problema, puedes intentar diferentes formatos de codificación, como encoding='ISO-8859-1', encoding='cp1252', etc.".

- Una vez aplicado el código dado por GPT, finalmente la base de datos mostró un ticket verde al reproducirlo, lo cual me indicaba que funcionaba.

- Realizo los siguientes códigos para obtener información inicial sobre la base de datos: 

print(df.head()) #para ver las primeras filas de la tabla.

print(df.describe()) #resumen estadístico de las variables numéricas.

print(df.info()) #información sobre las columnas y tipos de datos

### A raíz de esta información, percibo que existen varios valores nulos en la database. Reconocidos como "non-null" y "NaN". 

Asimismo, reconocemos qué datos contiene la tabla. En este caso, vemos que cuenta con datos como: sexo, edad, país, estimación, región y comuna. También hay "RAA_REGULAR" y "RAA_IRREGULAR", los cuales no reconozco por completo su significado pero distingo que puede tratarse de la situación de residencia del extranjero. 

- Por consiguiente, ejecutamos el siguiente código para verificar los datos faltantes en la base de datos: 

print(df.isnull().sum())

Este nos da la cantidad de valores faltantes en cada columna. En la columna de "Región", se percibe un número de 3.595 datos faltantes. Sin embargo, esta base de datos buscaba arrojarnos datos sobre la distribución por comuna, por lo que no nos interesa tanto la región. 

- Aquí debemos decidir qué haremos con los valores faltantes. La cantidad es no menor en algunas filas, sin embargo las filas que nos interesan, tienen 0 datos faltantes, por lo que borraremos directamente todas las filas con datos faltantes. Para ello utilizaremos el código:

df_clean = df.dropna()

- Los datos duplicados no son problema, pues es normal en columnas como; edad, sexo o país, que se repitan datos. 

- Tampoco nos interesa renombrar columnas, pues ya tienen nombres facilmente reconocibles. 

- Por el momento, procederemos a guardar la nueva base de datos con el código: 

clean_file_path = '/content/drive/My Drive/GRAFICA/base-2022-comunas-limpio.csv'

df_clean.to_csv(clean_file_path, index =False)

### Preguntas que podemos hacernos a raíz de la base de datos:

1. ¿Cuál es la distribución de la población extranjera por comuna?

1. ¿Cuál es la comuna en la que se mayor y menor concentración de extranjeros?

1. ¿Cuáles son los países de origen más comunes para la población extranjera en Chile?

1. ¿En qué año se percibió una mayor llegada de extranjeros?







