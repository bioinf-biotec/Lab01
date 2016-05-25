# Laboratorio 05 - Metagenómica
-------------------------

#### En este laboratorio vamos a familiarizarnos con la plataforma MG-RAST para el análisis de metagenomas.  
[MG-RAST](http://metagenomics.anl.gov) (metagenomics Rapid Annotation using Subsystem Technology) es una plataforma en linea de libre acceso que provee un conjunto de herramientas para el análisis y la visualización de metagenomas.  También, MG-RAST funciona comobase de datos donde los usuarios pueden alojar sus datos metagenómicos de manera pública o privada.  

#### Plataforma MG-RAST y exploración de metagenomas

Comencemos por ir a la página donde vamos a trabajar hoy día

- Ve a MG-RAST [aquí](http://metagenomics.anl.gov). Si no estás usando Mozilla te va a aparecer un aviso odioso que dice que el sitio ha sido optimizado para ese explorador. En la práctica no debería haber problemas con usar Safari o Chrome.  

![mgrast](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/mgrast.png)

- Dirígete hacia el ícono del planeta tierra en la esquina superior derecha  
- La página resultante muestra una tabla con funciones básicas de búsqueda y filtrado. Tómate unos minutos para explorar la tabla y darte una idea de qué tipos de muestras están disponibles para análisis.  
- Ahora vamos a ubicar y examinar dos proyectos metagenoma del [JVCI Global Ocean Sampling Expedition](http://www.jcvi.org/cms/research/projects/gos/).  
- Usando las casillas de búsqueda en la tabla, ubica y selecciona la muestra tomada del sitio de buceo [Dirty Rock](http://www.divesitedirectory.com/dive_site_costa_rica_cocos_reef_dirty_rock.html) en las Islas Cocos de Costa Rica.  

![dirtyrock](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/dirtyrock.png)


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

Dentro de la página para la muestra Dirty Rock, haz clic en el ícono de gráfico de barras donde dice "Analyze".  Deberías ver una ventana con las opciones como aparecen abajo.  

![analyze](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/analyze.png)  

- Asegúrate de que el e-value esté configurado en -10 y selecciona la visualización de gráfico de barras (la primera).  
- Haz clic en "Generate"  
- Cuando tu análisis termine, deberías ver una nueva pestaña que dice "Organism barchart 1"  
- Una vez que aparezca el gráfico de barras, haz clic en Bacteria. La distribución de Fila (Phylum) será visible  


**Responde las siguientes preguntas asociadas al análisis:** 

		¿Cuántas secuencias mapearon en contra de Proteobacteria? (Usa la opción Redraw para usar reads en vez de proporciones (raw)) 
		¿Cuántas secuencias de Salmonella ( Proteobacteria; Gammaproteobacteria; Enterobacteriales; Enterobacteriaceae) fueron identificadas?
		
#### Trabajo de laboratorio para la próxima semana

El trabajo de laboratorio para la próxima semana consta de dos partes. La primera parte ya la tienes lista. Simplemente tienes que responder las preguntas que aparecen a través de esta guía y enviar un informe a <bioinformatica.unab2016@gmail.com> NO al profesor! Envien a este correo los informes hasta el jueves de la semana siguiente a la realización del práctico. La hora límite es las 23:59.
En el Asunto del correo pongan Informe de Laboratorio 0x así nosotros podemos clasificar automáticamente los informes. Para la próxima semana el Asunto del correo debería ser Informe de Laboratorio 04.

|**Profesor**|**Nombre**|**Correo electrónico**|  
| ------------- |:-------------:| -----:|
|Profesor responsable | Dr. Eduardo Castro Nallar |eduardo.castro@unab.cl|  
|Profesor ayudante sección 1  | Ingrid Araya Durán |ingrid.araya.duran@gmail.com|  
|Profesor ayudante sección 1  |Sandro Valenzuela | sandrolvalenzuelad@gmail.com|  
|Profesor ayudante sección 2  |Javier Cáceres | ja.caceresmolina@gmail.com|  
|Profesor ayudante sección 2  |Consuelo Bello | consuelobelloz@gmail.com|  

La segunda parte tiene que ver con leer el artículo Jansson J, Field D, Fierer N, et al. ***Unlocking the potential of metagenomics through replicated experimental design***. Nature Publishing Group. 2012;30(6):513-520. doi:10.1038/nbt.2235.  

Puedes acceder al artículo [aquí](https://github.com/bioinf-biotec/labs_bioinf/raw/master/Knight_2012.pdf). Recuerda que el contenido de este artículo es el material para el próximo control de entrada.


