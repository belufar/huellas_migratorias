## ANELISSE LIMA

### PASO A PASO

- Hice una búsqueda de un archivo csv en la página del Instituto Nacional de Estadísticas de Chile y procedí a descargarla. Elegimos esa fuente porque es de caracter oficial y contiene datos confiables y recientes. Elegí el archivo porque está relacionado a la estimación de población extranjera en 2022 segmentada por regiones. 

- Abrí Google Colab, un notebook nuevo, lo vincule con mi drive y puse el siguiente código: 

from google.colab import drive
drive.mount('/content/drive')

- Después escribí: "import panda as pd" para que importe la biblioteca de Pandas y sea más fácil el uso de las funciones que usare en el notebook. 

- Posteriormentes escribí la #Ruta al archivo CSV en tu Google Drive

file_path = '/content/drive/MyDrive/Colab Notebooks/base-2022-regiones.csv'

- #Especificar la codificación al leer el archivo CSV

df = pd.read_csv(file_path, encoding='ISO-8859-1')

"En este caso, he utilizado encoding='ISO-8859-1', que es otro formato de codificación comúnmente utilizado. Sin embargo, si este no resuelve el problema, puedes intentar diferentes formatos de codificación, como encoding='cp1252'".

- Tuve algunos problemas al visualizar los primeros registros del DataFrame porque chatGPT me daba el código: 
print(datos.head()) 

Cuando ejecutaba el código me aparecía que "datos" no estaba identificado, entonces me mandó el siguiente código:           print(df.head()) y se resolvió el problema. Solo requería cambiar "datos" por "df".

- Una vez aplicado el código dado por GPT, finalmente la base de datos funcionó

- Escribí los siguientes códigos para obtener información inicial sobre la base de datos: 

print(df.head()) #para ver las primeras filas de la tabla.

print(df.describe()) #resumen estadístico de las variables numéricas.

print(df.info()) #información sobre las columnas y tipos de datos

### FUENTE DE DATOS UTILIZADOS

- La base de datos cuenta con datos como: sexo, edad, país, estimación, región, comuna, RAA_REGULAR y RAA_IRREGULAR 

- Al encontrar varios valores reconocidos como "non-null" y "NaN", se ejecutó el siguiente código para verificar los datos faltantes en la base de datos: 

print(df.isnull().sum())
 
- Se decidió borrar directamente todas las filas con datos faltantes ya que se consideró que sería para la mejor comprensión de los datos. Como la investigación está vinculada con los efectos sociales de la migración, quitar los datos faltantes facilitarán la comprensión al momento de graficar los datos. Para ello se utilizó el código:

df_clean = df.dropna()

- Se consideró que los datos duplicados no sería problema, pues es normal en columnas como; edad, sexo o país, que se repitan datos. 

- Se optó por mantener los nombres de las columnas ya que son de fácil comprensión.

- Por último, se guardó la nueva base de datos con el código: 

clean_file_path = '/content/drive/My Drive/Colab Notebook/base-2022-comunas-limpio.csv'

df_clean.to_csv(clean_file_path, index =False)

### PREGUNTAS A PARTIR DE LA BASE DE DATOS 

- ¿Cuáles son las regiones con más alto índice de migración?

- ¿Qué países predominan en las regiones con más alto indice de migración?

- ¿Qué sexo migra más en las regiones donde hay más alto índice de migración?

- ¿Qué rango de edad migra más en las regiones donde hay más alto índice de migración?