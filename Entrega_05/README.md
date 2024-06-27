# README

En el siguiente README se encuentran los links a la presentación así como la autoría de lo que hizo cada integrante del grupo y su documentación de proceso respectiva. 

[Link al video presentación](insertar link)
[Link al pdf](insertar link)


Ponderador de Autoría:

Belén Farías:
    - Propuesta visualizaciones atomicas
    - Decisiones elementos visuales
    - código (index, style, script)

Anelisse Lima:
    -Analisis hipotesis 
    -Propuesta diseño información
    -Crónica



# Documentación de proceso: Belén Farías

Primero, confeccioné nuestra base de datos. A raíz de datos y estadísticas esparcidos dados por el Servicio Nacional de Migraciones. Ante esto, encontramos datos interesantes no solo sobre cómo se distribuyen demográficamente los migrantes, sino también las razones para migrar a Chile, su situación económica, laboral, estudios, educacional, e incluso sobre sus relaciones en el país. Es decir, información sobre cuántos reportaban haberse sentido discriminados, en que lugares y quienes señalan no conocer a ninguna persona donde viven actualmente. 

Con estos datos, logramos darnos una imagen general al camino del migrante en Chile. Por lo que la idea de qué abordaría la webstory estaba más clara ahora. 

Comencé decidiendo cómo debía verse el webstory. Puesto que para el encargo pasado, este fue corregido. En base a estas correcciones, decidimos cambiarlo por un estilo más orgánico. En una hoja de papel trazé cómo quería que se contara esta hisotira. Resultó más fácil que hacerlo en formato Wireframe en Canva. Así el nuevo estilo trazaría "el camino de los migrantes". Puesto que el proyecto se llama Huellas Migratorias, se decidió hacer cómo si estuvieramos siguiendo a los migrantes desde su punto de origen. Así pues, la información se desglosaría de la siguiente forma:

    - Razón para dejar el país de origen: Aquí se expondría la información con los datos y estadísticas de por qué cierto grupo de migrantes decidió dejar su país de origen. 
    - ¿Por qué Chile?: Ya que sabemos por qué migran, ahora entenderíamos por qué eligen Chile como su país de origen. 
    - Distribución regional: Ya sabiendo sus motivaciones, ahora podemos ver cómo se han ido distribuyendo a lo largo de Chile, y en qué regiones se concentran qué nacionalidades. Este gráfico también ayuda a entender porqué la mayoría de las estadísticas están centradas en Bolivia, Colombia, Haití, Perú y Venezuela. Puesto que son las nacionalidades con mayor concentración a lo largo del país. 
    - Distribución venezolanos vs el resto: El gráfico anterior resulta llamativo por el hecho de que gran parte de las regiones están más concentradas por migrantes venezolanos. Por lo que se pondría información sobre la distribución de las personas de Venezuela en Chile versus otras nacionalidades. 
    - Discriminación: Ya una vez sabemos sus motivos y dónde están ubicados, cabe preguntarnos, ¿cómo los ha recibido el país de destino? En este caso, con estadísticas sobre el porcentaje de migrantes que señalan haber sufrido algún tipo de discriminación por su nacionalidad u otro motivo. 
    -Relaciones: Finalmente, en la misma línea de la información anterior, se entrega información sobre el porcentaje de migrantes que señalan que no conocen a ninguna persona donde viven acutalmente. 

El storyline que se demarcó sigue una misma linea, que es de alguna forma el camino de un migrante desde su origen y motivaciones para migrar, dónde decide asentarse y cómo se siente una vez en el país de origen. 

Por consiguiente, ya una vez decidido esto, se procede a sistematizar los gráfico que queremos mostrar en nuestra webstory, esto quiere decir, convertirlos en csv y procesarlos en Google Colab. En este caso, tuvimos la suerte de contar con tablas simples, por lo que el proceso fue sencillo. En mi caso particular, me encargué de hacer los gráficos para la información relacionada a cómo se distribuían por región, por qué eligen Chile y sobre las relaciones interpersonales. En este caso, realicé en python el gráfico de demografía regional, sin embargo era un poco soso, por lo que decidí traspasarlo a fluorish para darle un gráfico más creativo. 

Por otro lado, el gráfico de los motivos para elegir Chile, decidí realizarlo con python. Fue sencillo de hacer siguiendo los mismos pasos del encargo anterior para realizar visualización atómica. De hecho, lo hice en el mismo cuaderno, por lo que pueden revisar todo el proceso ahí. Por supuesto, con mucha ayuda de Chat Gpt, pues el programa muchas veces me arrojaba error por temas de formato en su mayoría. 

Finalmente, el gráfico de relaciones interpersonales, decidí hacerlo en Flourish para utilizar un tipo de gráfico más complejo; un diagrama de Sankey. Se traspasó la tabla de la base de datos a Flourish (de manera manual, por suerte no eran macro datos). 

Por consiguiente, ya con los gráficos, procedí a crear el html para la página web. Mis pocas capacidades con este lenguaje me llevaron a pedirle ayuda a Chat GPT para partir por una base. Le di toda la información sobre nuestra identidad visual; tipo de letra a usar (Roboto), nuestra paleta de colores, y cómo quería que se distribuyera la información con tal de que yo pudiera ir rellenando luego a mi gusto. Fue un proceso complicado puesto que me costó comunicarme bien con GPT para que me diera exactamente lo que quería. Por lo que me conformé con un esqueleto simple y comencé a trabajar desde ahí. Editando el logo y adjuntando los html de los gráficos. 

Resultó particularmente dificil entender cómo mover los gráficos de lugar, agrandarlos y elegir exactamente en qué parte de la página quería que estuvieran, sobretodo aquellos que iban en iframe desde Flourish. Hasta que, jugando con los valores, entendí que esa información se edita desde el style.css en el código que se forma así, notando que entre el html y el css podía saber qué nombre tendría la visualización que quería mover:

### .visualization.centered {
    width: 100%;
    height: 800px;
    margin: 0 auto;
}

### .visualization.centered iframe {
    width: 100%;
    height: 800px;
    margin: 0 auto;
}

-------------

Por consiguiente, decidí cambiar la fuente por una que no está por defecto y que tuve que instalar. Pero fue más fácil de lo que pensé. Bastó con ver un tutorial en Youtube. Simplemente había que ir a [Google Fonts](https://fonts.google.com/selection/embed) y allí de hecho te dan todos los códigos para importarla en un css. Con eso también aprendí a seleccionar un tipo de letra distinta para el title, el h1 y el p.  

Ya una vez ajustado todo y puestos los gráficos. Procedí a escribir la información que se daría para cada texto. Siguiendo muy de la mano lo escrito en la crónica por mi compañera Anelisse. 

Además, cree gifs de huellas para darle un cierto dinamismo a la lectura. Los coloqué entre cada sección para que fuese una especie de "guía" de la mirada del lector. Utilizando de base lo que fui viendo de los scripts del grupo de música urbana, también me ayudé con chat GPT para ir acomodando correctamente los gifs. 

El resto fue ir afinando detalles, bordes, nombres. Y el esqueleto quedó más armado :) 

#### PD: Algo que aprendí y no recuerdo haberlo escuchado en clases, fue cuando noté que el logo no me cargaba a pesar de estar correctamente enrutado. Gracias a Youtube noté que era porque al escribir la ruta, si estas enlazando algo que está en la misma carpeta que tu index, a veces poner un . delante de la ruta, hace toda la diferencia, por ejemplo: ./imagenes/logo.png (lo mismo me sirvió para los gráficos, pues no se veían hasta que puse el punto). 