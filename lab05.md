![cbibunab](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/unabcbibhorizontal.png?raw=true)

# Laboratorio 05 - Metagenómica
-------------------------

#### En este laboratorio vamos a familiarizarnos con la plataforma MG-RAST para el análisis de metagenomas.  
[MG-RAST](http://metagenomics.anl.gov) (metagenomics Rapid Annotation using Subsystem Technology) es una plataforma en línea de libre acceso que provee un conjunto de herramientas para el análisis y la visualización de metagenomas.  También, MG-RAST funciona como base de datos donde los usuarios pueden alojar sus datos metagenómicos de manera pública o privada. 

#### Plataforma MG-RAST y exploración de metagenomas

Comencemos por ir a la página donde vamos a trabajar hoy día.

- Ve a MG-RAST [aquí](http://metagenomics.anl.gov).  

![mgrast](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/mgrast.png?raw=true)

- Haz clic en **search**. 
- La página resultante muestra una tabla con funciones básicas de búsqueda y filtrado. Tómate unos minutos para explorar la tabla y darte una idea de qué tipos de muestras están disponibles para análisis.
- Ahora vamos a ubicar y examinar dos proyectos metagenoma del [JVCI Global Ocean Sampling Expedition](http://www.jcvi.org/global-ocean-sampling-expedition-gos).
- Usando las casillas de búsqueda en la tabla, ubica y selecciona la muestra tomada del sitio de buceo [Dirty Rock](http://www.divesitedirectory.com/dive_site_costa_rica_cocos_reef_dirty_rock.html) en las Islas Cocos de Costa Rica.  

![dirtyrock](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/dirtyrock.png?raw=true)


**Responde las siguientes preguntas asociadas a la muestra:**  
		
		¿Cuántas secuencias fueron subidas? 
		¿Qué tipo de plataforma de secuenciamiento fue usada para producir estos datos?
		¿Cuántas secuencias pasaron el control de calidad? ¿A qué crees que se refiere esto?
		¿Cuántos otros metagenomas están disponibles para el bioma “marine habitat”?
		¿Cuántas reads fueron asignadas a eucariontes según MG-RAST?
		¿Cuál es el filo (Phylum) más abundante en la muestra?
		¿A cuántas secuencias se les asignó una función de acuerdo a la base de datos KEGG con un e-value entre -10 y -20?
		¿Por qué hay tan pocas secuencias con funciones asignadas según SwissProt?

#### Análisis de metagenomas

Dentro de la página para la muestra Dirty Rock, en la parte superior, haz clic en el ícono de gráfico de barras "analysis".

![analyze](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/analysis.png?raw=true)  

- En el menú desplegable del buscador selecciona "ID", luego escribe el ID del proyecto "mgm4441593.3" y selecciona el set de datos.
- Haz clic en el ícono `>`, luego haz clic en el ícono verde y espera.
- Haz clic en el ícono de grafico de barras que aparece abajo.
- En el menú desplegable "level" selecciona "phylum". La distribución de Fila (Phylum) será visible.
- En las opciones de visualización haz clic en "table" y podrás ver la tabla detallada a partir de la que se genero el gráfico de barras.


**Responde las siguientes preguntas asociadas al análisis:** 

		¿Cuántas secuencias mapearon en contra de Proteobacteria?
		¿Cuántas secuencias de Salmonella (Proteobacteria; Gammaproteobacteria; Enterobacteriales; Enterobacteriaceae) fueron identificadas? (Pista: level - genus)
		
#### Trabajo de laboratorio para la próxima semana

El trabajo de laboratorio para la próxima semana consta de dos partes. La primera parte ya la tienes lista. Simplemente tienes que responder las preguntas que aparecen a través de esta guía y enviar un informe al ayudante <mendez.katterinne@gmail.com>. Envíen a este correo los informes hasta el miércoles de la semana siguiente a la realización del práctico. La hora límite es las 23:59.
En el Asunto del correo pongan Informe de Laboratorio 0x así nosotros podemos clasificar automáticamente los informes. Para la próxima semana el Asunto del correo debería ser Informe de Laboratorio 05.

La segunda parte tiene que ver con leer el artículo Jansson J, Field D, Fierer N, et al. ***Unlocking the potential of metagenomics through replicated experimental design***. Nature Publishing Group. 2012;30(6):513-520. doi:10.1038/nbt.2235.  

Puedes acceder al artículo [aquí](https://github.com/bioinf-biotec/labs_bioinf/raw/master/nbt.2235.pdf). Recuerda que el contenido de este artículo es el material para el próximo control de entrada.
