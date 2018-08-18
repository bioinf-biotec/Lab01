# Laboratorio 04 - Filogenética Molecular ![](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/tree.png?raw=true)

#### En este laboratorio vamos a familiarizarnos con la plataforma Phylogeny.fr para la inferencia de filogenias usando distintos métodos. Sigue las instrucciones y responde las preguntas, entre `[]` se indica el puntaje asignado a cada pregunta. Tus respuestas van a formar parte de la nota de laboratorio 04.

### Plataforma Phylogeny.fr y preparación de datos

Comencemos por ir a la página donde vamos a trabajar hoy día.

- Ve a **Phylogeny.fr** [aquí](http://www.phylogeny.fr/index.cgi).

![phylofr](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/phylofr.png?raw=true)

- Navega dentro del portal siguiendo vínculos a, por ejemplo, "_Phylogeny analysis_", "_Online programs_" y finalmente a "_Documentation_".

---  

**1.** ¿Qué ofrece o para qué sirve el portal Phylogeny.fr? [2]

**2.** Nombra y explica brevemente los 3 modos en los que se puede ejecutar el pipeline de Phylogeny.fr. [2]

**3.** Menciona qué tipos de análsis se pueden realizar en el portal de acuerdo a la documentación. (_Online Programs_) [2]

---

En este laboratorio vamos a usar los genes SRY que colectaste algunas clases atrás en el laboratorio de alineamiento. Ve a la parte 1 del [laboratorio 02](https://github.com/bioinf-biotec/labs_bioinf/blob/master/lab02.md) y obtén un archivo con las secuencias del mRNA del gen SRY. De todas maneras, puedes copiar las secuencias [acá](https://github.com/bioinf-biotec/labs_bioinf/raw/master/documents/SRY_orthologs_mRNAs.fasta).

Tu misión es inferir dos filogenias. La diferencia estará en los programas que usarás a través de la pipeline de Phylogeny.fr, para el alineamiento múltiple, curación del alineamiento, construcción del árbol filogenético, y posterior visualización de éste.

- Dirígete a "_Phylogeny Analysis_" y selecciona el modo "_A la Carte_".

![alacarte](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/alacarte.png?raw=true)

- Una vez en "_Workflow Settings_", en la casilla "_Name of the analysis_" escribe tu nombre completo (para que tu nombre aparezca en las capturas de pantallas de las filogenias que obtengas).
- Para tu **filogenia número 1** selecciona: `ProbCons`, `GBlocks`, `MrBayes`, y `TreeDyn`.
- Para tu **filogenia número 2** selecciona: `ClustalW`, `Remove positions with gaps`, `TNT`, y `TreeDyn`.

---

**4.** Incluye en tu informe una captura de pantalla de las dos filogenias que inferiste. Recuerda que tu nombre completo debe aparecer en la imagen de cada filogenia (_Name of the analysis_). [2]

**5.** ¿A qué se refiere el paso de _Alignment curation_ y para qué sirve? [3]

**6.** ¿Cuál es la diferencia entre BioNJ y Neighbor? [3]

**- Corre nuevamente ambas filogenias, pero esta vez sin seleccionar _Alignment curation_.**

**7.** Incluye en tu informe una captura de pantalla de las dos filogenias que inferiste (sin _Alignment curation_). Recuerda que tu nombre completo debe aparecer en la imagen de cada filogenia (_Name of the analysis_). [2]

**8.** ¿Cuál es el efecto de no hacer la curación del alineamiento en las filogenias? [3]

**9.** Describe las diferencias entre las filogenias que has estimado (4 en total): cantidad de grupos monofiléticos, relaciones que potencialmente cambiaron, etc. [5]

---

##### No olvides enviar tu informe de laboratorio al correo electrónico de la profesora ayudante: kat.mendez@uandresbello.edu. Tienes plazo hasta las 23:59 hrs del día jueves de la semana siguiente.
##### También, recuerda estudiar las lecturas designadas para la próxima semana. Puedes revisarlas en "Controles de entrada y lecturas" de la página del curso, [aquí](https://github.com/bioinf-biotec/labs_bioinf). 

---

<p align="center">
<img width="50%" src="https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/unab_cbib_horizontal.png?raw=true">
</p>

