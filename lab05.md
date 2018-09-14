# Laboratorio 05 - Metagenómica

#### En este laboratorio vamos a familiarizarnos con la plataforma MG-RAST para el análisis de metagenomas. Sigue las instrucciones y responde las preguntas, entre `[]` se indica el puntaje asignado a cada pregunta. Tus respuestas van a formar parte de la nota de laboratorio 05.

[MG-RAST](http://metagenomics.anl.gov) (metagenomics Rapid Annotation using Subsystem Technology) es una plataforma en línea de libre acceso que provee un conjunto de herramientas para el análisis y la visualización de metagenomas.  También, MG-RAST funciona como base de datos donde los usuarios pueden alojar sus datos metagenómicos de manera pública o privada. 

### Plataforma MG-RAST y exploración de metagenomas

Comencemos por ir a la página donde vamos a trabajar hoy día.

- Ve a MG-RAST [aquí](http://metagenomics.anl.gov).  

![mgrast](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/mgrast.png?raw=true)

- Haz clic en **search**. 
- La página resultante muestra una tabla con funciones básicas de búsqueda y filtrado. Tómate unos minutos para explorar la tabla y darte una idea de qué tipos de muestras están disponibles para análisis.
- Ahora vamos a ubicar y examinar dos proyectos metagenoma del [JVCI Global Ocean Sampling Expedition](http://www.jcvi.org/global-ocean-sampling-expedition-gos).
- Usando las casillas de búsqueda en la tabla, ubica y selecciona la muestra tomada del sitio de buceo [Dirty Rock](http://www.divesitedirectory.com/dive_site_costa_rica_cocos_reef_dirty_rock.html) en las Islas Cocos de Costa Rica.  

![dirtyrock](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/dirtyrock.png?raw=true)

---
Responde las siguientes preguntas asociadas a la muestra:
		
**1.** ¿Cuántas secuencias fueron subidas? [1]

**2.** ¿Qué tipo de plataforma de secuenciamiento fue usada para producir estos datos? [2]

**3.** ¿Cuántas secuencias pasaron el control de calidad? ¿A qué crees que se refiere esto? [3]

**4.** ¿Cuántos otros metagenomas están disponibles para el bioma “marine habitat”? [1]

**5.** ¿Cuántas reads fueron asignadas a eucariontes según MG-RAST? [1]

**6.** ¿Cuál es el filo (Phylum) más abundante en la muestra? [1]

**7.** ¿A cuántas secuencias se les asignó una función de acuerdo a la base de datos KEGG con un e-value entre -10 y -20? [1]

**8.** ¿Por qué hay tan pocas secuencias con funciones asignadas según SwissProt? [2]

---

### Análisis de metagenomas

Dentro de la página para la muestra Dirty Rock, en la parte superior, haz clic en el ícono de gráfico de barras "analysis".

![analyze](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/analysis.png?raw=true)  

- En el menú desplegable del buscador selecciona "ID", luego escribe el ID del proyecto "mgm4441593.3" y selecciona el set de datos.
- Haz clic en el ícono `>`, luego haz clic en el ícono verde y espera.
- Haz clic en el ícono de grafico de barras que aparece abajo.
- En el menú desplegable "level" selecciona "phylum". La distribución de Fila (Phylum) será visible.
- En las opciones de visualización haz clic en "table" y podrás ver la tabla detallada a partir de la que se genero el gráfico de barras.

---
Responde las siguientes preguntas asociadas al análisis:

**9.** ¿Cuántas secuencias mapearon en contra de Proteobacteria?

**10.** ¿Cuántas secuencias de Salmonella (Proteobacteria; Gammaproteobacteria; Enterobacteriales; Enterobacteriaceae) fueron identificadas? (Pista: level - genus)

---

##### No olvides enviar tu informe de laboratorio al correo electrónico de la profesora ayudante: kat.mendez@uandresbello.edu. Tienes plazo hasta las 23:59 hrs del día jueves de la semana siguiente.
##### También, recuerda estudiar las lecturas designadas para la próxima semana. Puedes revisarlas en "Controles de entrada y lecturas" de la página del curso, [aquí](https://github.com/bioinf-biotec/labs_bioinf). 

---

<p align="center">
<img width="50%" src="https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/unab_cbib_horizontal.png?raw=true">
</p>


