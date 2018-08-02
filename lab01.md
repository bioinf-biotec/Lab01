# Laboratorio 01 - Bases de datos biológicas ![](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/big-data.png?raw=true)

#### En este laboratorio vamos a explorar bases de datos biológicas a través de un ejemplo guiado. El objetivo del práctico es que uses y te interiorices con la mayor parte de las herramientas que las bases de datos te pueden ofrecer. Sigue las instrucciones y responde las preguntas, entre `[]` se indica el puntaje asignado a cada pregunta. Tus respuestas van a formar parte de la nota de laboratorio 01.

### Parte 1: Enfermedades genéticas y genes

- Busca una enfermedad **genética** humana en alguna base de datos de literatura, i.e., [Pubmed](http://www.ncbi.nlm.nih.gov/pubmed/), [Google Scholar] (https://scholar.google.com), o en bases de datos de enfermedades genéticas, e.g., [OMIM](http://www.omim.org).

---

**1.** Nombra y describe brevemente la enfermedad que escogiste, qué la causa y cuáles son sus consecuencias. [3]

**2.** ¿Cuál(es) gene(s) han sido relacionados con esta enfermedad? [1]

---

##### Ve a la NCBI Gene database ([http://www.ncbi.nlm.nih.gov/gene](http://www.ncbi.nlm.nih.gov/gene)) y busca el gen que está involucrado en la enfermedad seleccionada. Algunos ejemplos pueden ser CFTR, SGCG, IDDM3, HBB. También puedes tratar directamente con el nombre de una enfermedad o condición (e.g., duchenne muscular dystrophy).   

![ncbi_gene1](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/ncbi_gene1.png?raw=true)

La base de datos de genes de NCBI concentra información de distintas fuentes para producir una "ficha" con vínculos a otras bases de datos. Fíjate en el índice al lado derecho de la pantalla "_Table of contents_", te ayudará a encontrar la información que buscas rápidamente.

![ncbi_gene2](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/ncbi_gene2.png?raw=true)

---  
		
**3.** ¿Tiene nombres alternativos el gen? ¿Cuáles? [1]

**4.** ¿En qué cromosoma está? ¿Cuántos exones tiene? [1]

**5.** ¿Cuántas isoformas de transcritos? [2]

**6.** ¿Qué tipo de proteina es codificada por este gen? ¿Cuál es su número EC? [2]

**7.** ¿Qué genes están inmediatamente río arriba/abajo? [1]

---

De tus conocimientos de genética básica, probablemente ya sabes que un gen puede tener múltiples alelos, y a su vez estos alelos pueden estar asociados a distintos fenotipos, e.g., enfermedades, severidad, etc. En la página de tu gen, dirígete a la sección "_Variation_" -> selecciona "_See variants in ClinVar_" e identifica cuántas variantes génicas tiene tu gen y a qué tipo de sustituciones corresponden. Fíjate que en la parte izquierda de la página hay un menú para filtrar datos, por ejemplo, por tipo de variación ("_Variation type_").

---

**8.** ¿Cuál es la longitud de tu gen? [2]

**9.** ¿Cuántas variantes de tu gen hay descritas y qué tipo de variantes son? [2] 

**10.** ¿Las sustituciones (i.e. cambio de un nucleótido) corresponden a cambios sinónimos o no sinónimos? [2]

**11.** ¿Existen ortólogos de tu gen en otras especies? ¿Cuántos? [1]

**12.** ¿Y paralógos? ¿Hay pseudogenes? ¿Cuántos? [1]

---

### Parte 2: Rutas y procesos metabólicos

Los genes generalmente codifican proteínas, las cuales, a su vez están involucradas en rutas y procesos metabólicos. Existen bases de datos especializadas que compilan información referente a metabolismo. Las más populares son [BioCyc](http://biocyc.org), [REACTOME](http://www.reactome.org), y [KEGG](http://www.kegg.jp). Otras bases de datos agrupan proteínas involucradas en procesos biológicos más gruesos como [Clusters of Orthologous Groups (COGs)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4383993/) o [Gene Ontology (GO)](http://geneontology.org). Visita los vínculos a estas páginas y familiarízate con sus funcionalidades (no más de 10 minutos).

Ahora sigamos trabajando con el gen que escogiste en la parte 1. Una vez en la página principal de KEGG, haz clic en el vínculo KEGG GENES. 
Para buscar el gen que escogiste en KEGG GENES, en "_Enter org:gene_" tienes que escribir el código del organismo (para *Homo sapiens* es "hsa") y el nombre del gen en minúscula (por ejemplo: gapdh), separados por ":", así: "hsa:gapdh".

![kegg_genes1](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/kegg_genes1.png?raw=true)

Haz clic en "_Entry_", se abrirá una ventana donde encontrarás un montón de información. Revisa esta información para responder las siguientes preguntas.

---

**13.** Anteriormente encontraste nombres alternativos de tu gen ¿Existen otros reportados por KEGG? ¿Cuáles? [1]

**14.** ¿Cuál es el número de identificación de tu gen (_entry number_)? [1]

**15.** ¿En qué rutas metabólicas participa la proteína codificada por tu gen? [1]

**16.** En general, cada unidad dentro de una base de datos tiene un número o código de identificación único. De esta forma, uno puede obtener exactamente lo que quiere dentro de un oceano de otras cosas ¿En qué otras bases de datos está tu gen presente y cuáles son sus números de acceso? [1]

---

La figura más clásica que se puede obtener es el diagrama con una ruta metabólica. Probablemente tu gen está involucrado en más de una.

![pathway](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/pathway.png?raw=true) 

---

**17.** Escoge una ruta metabólica y seleccionala para ver el diagrama correspondiente, toma una captura de pantalla e incluyela en tu informe. [1]

**18.** ¿Qué significan los cuadros verdes en el diagrama? (Pista: haz clic en `Help`) [2]

**19.** ¿Con qué otra(s) ruta(s) se cruza la ruta metabólica que escogiste? [2]

---

Ahora vamos a la página de [Gene Ontology (GO)](http://geneontology.org). Una ontología es un tipo de anotación genómica que teine que ver con atributos de regiones genómicas o de genes. En este sentido, el gen del citocromo c, por ejemplo, no es parte de GO pero su actividad biológica, i.e., su atributo, si está (oxidoreductasa). Cualquier persona que quiera hacer un experimento de transcriptómica o genómica, secuenciar un genoma de un organismo, etc. debería tener un entendimiento profundo sobre GO. Un buen comienzo es [este artículo](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003343#s2) en PLOS Computational Biology.

Ahora, desde el website de GO, lee la documentación para poder responder las siguientes preguntas:

---  

**20.** ¿Cuáles son las principales ontologías o dominios que conforman Gene Ontology? [2]

**-** Ve a "_Tools_" --> "_AmiGO 2_" y escribe en la casilla de búsqueda: "GO:0006096".  

**21.** ¿A qué corresponde este término y qué otra información te entrega la página? [3]

**-** Haz clic en "Graph Views" y examina el gráfico.

**22.** Escribe 10 categorías GO a la cual GO:0006096 pertenece. [2]

---

![go](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/go.png?raw=true)

### Parte 3: Descargando secuencias, convirtiendo formatos

De alguna u otra forma, probablemente ya has tenido algún tipo de interacción con NCBI descargando secuencias nucleotídicas o aminoacídicas. En esta sección nos vamos a enfocar en descargar secuencias y sus números de acceso.

Ve a la página de [NCBI](http://www.ncbi.nlm.nih.gov) y selecciona la base de datos de nucleótidos. En la casilla de búsqueda escribe GAPDH y presiona Enter.

---

**23.** ¿Cuántos items fueron encontrados? ¿cuántos en animales? [1]

**-** Probablemente tus resultados fueron una mezcla de fragmentos de genes, regiones codificantes parciales, genes completos, etc. Filtra tus datos por mRNA, animales, RefSeq. Haz clic en la entrada para la secuencia de GAPDH de _Danio rerio_. 
		
**24.** ¿Cuál es la longitud del gen? [1]
		
**25.** ¿Cuál es la referencia bibliográfica más reciente? [1]

**26.** ¿Cuál es el número de acceso? [1]

**27.** Descarga la secuencia en formato [FASTA](http://www.bioinformatics.nl/tools/crab_fasta.html) y agrégala a tu informe. [1]

---

![gapdh_fasta](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/gapdh_dr_fasta.png?raw=true)

Como nota adicional, la interfaz gráfica de NCBI no es de mucha ayuda cuando tienes que descargar muchas secuencias o genomas completos. En este caso se recomienda usar el portal FTP de NCBI: [ftp.ncbi.nlm.nih.gov](ftp://ftp.ncbi.nlm.nih.gov/)

Para finalizar esta parte, vamos a convertir la secuencia que bajaste a otro formato. Existen muchos formatos de secuencias porque responden a distintos atributos que sus autores consideraron importantes de registrar y también por razones históricas. Uno de los formatos más usados es el FASTA, sin embargo en filogenética uno súper popular y requerido por muchos programas es el formato [NEXUS](https://en.wikipedia.org/wiki/Nexus_file).

---

**-** Ve a la página de [Seqret](http://www.ebi.ac.uk/Tools/sfc/emboss_seqret/) del EBI, que contiene una herramienta online útil para re-formatear secuencias. Copia y pega la secuencia en formato FASTA de GAPDH en la casilla. Recuerda seleccionar correctamente el tipo de secuencia y formato de salida requerido. Haz clic en "Submit".

**28.** Adjunta la secuencia en formato NEXUS a tu informe. [1]

---

![gapdh_nexus](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/gapdh_dr_nexus.png?raw=true)

### Parte 4: Buscando artículos científicos en línea

Buscar literatura relativa a un tema científico no tiene que ser tedioso ni complicado. Al contrario, conociendo herramientas dedicadas para esto puede hacerte la vida muy simple.

En general, el primer impulso es buscar en los clásicos buscadores directamente. Sin embargo, el uso de alertas, tablas de contenido electrónicas, y por sobre todo modificadores de búsquedas en línea hacen que estar actualizado en tu tema de investigación sea algo instántaneo.

- Crea una cuenta gratuita en NCBI y Google Scholar.
- Escoge un área de investigación, e.g., bacterial genomics, human genetics, etc.
- Ahora crea una alerta de búsqueda en NCBI PubMed.

![pubmed_alert](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/pubmed_alert.png?raw=true)

---

**29.** En tu informe, incluye una captura de pantalla de tu alerta. Si es que recibes una alerta en tu correo electrónico, también puedes adjuntarla en tu informe. [1]

---

Las páginas de búsqueda clásicas son:

- [Pubmed](http://pubmed.com), [Google Scholar](https://scholar.google.com), [Scopus](http://www.scopus.com) para artículos científicos.
- [USPTO](http://www.uspto.gov), [ESPACENET](http://www.epo.org/searching-for-patents/technical/espacenet.html), [INAPI](http://www.inapi.cl/portal/institucional/600/w3-propertyvalue-877.html) para patentes. Google Scholar también permite filtrar resultados por patentes.

Ahora vamos a la página de la revista [Nature Genetics](http://www.nature.com/ng/index.html). El obejtivo es configurar una tabla de contenidos electrónica, i.e., que cada vez que la revista publique un número nuevo te llegue la tabla de contenidos de ese número a tu correo electrónico. Puedes encontrar el vínculo en la esquina superior derecha, ***E-alert***.

![ngen](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/ngen_ealert.png?raw=true)

---

**30.** En tu informe agrega una captura de pantalla de tu suscripción o del correo electrónico de confirmación. [1]

---

Para finalizar esta parte vamos a prácticar el uso de **operadores de búsqueda en Google Scholar**. Entra a [Google Scholar](https://scholar.google.com).

---

**-** Haz una búsqueda, por ejemplo, busca "Human Microbiome" (puedes buscar cualquier otro término).

**-** Ahora usa comillas para realizar tu búsqueda "Human Microbiome".
			
**31.** ¿Son los resultados idénticos o no? [1]

El uso de comillas restringe los resultados a resultados donde la frase que buscas aparece de manera exacta.

**-** También puedes usar `*` para representar una palabra que falta, e.g., "Human Microbiome" *.

**32.** ¿En qué cambiaron los resultados de la búsqueda? [1]

**-** También puedes condicionar tus búsquedas a rangos de números como precios, años, etc. Prueba escribiendo lo siguiente en google.com: 14 inch...17 inch laptops.

**33.** ¿Qué encuentras en los resultados? Prueba sin el rango también. [1]

**-** Para buscar artículos científicos también es útil restringir los resultados de búsqueda a tipos de archivo. Prueba escribiendo: "human microbiome" filetype:pdf.

**34.** Describe tus resultados. [1]

**-** Otro truco útil es usar signos `-` y `+`. Por ejemplo, trata buscar: "PCR amplification" +temperature. Y luego: "PCR amplification" -temperature.

**35.** ¿En qué cambian los resultados de la búsqueda? [1]

**-** Finalmente, prueba los operadores _Boolean_ que representan opciones de inclusión. Por ejemplo, trata con: Soil OR Human pathogens. Y luego trata con: Soil AND Human pathogens.

**36.** De nuevo, ¿en qué cambian los resultados de la búsqueda? [1]

Puedes seguir practicando tus habilidades para buscar artículos científicos. Los ejemplos de esta sección fueron tomados desde [acá](http://libguides.mit.edu/c.php?g=176061&p=1159432). 

##### No olvides enviar tu informe de laboratorio al correo electrónico de la profesora ayudante: kat.mendez@uandresbello.edu. Tienes plazo hasta las 23:59 hrs del día jueves de la semana siguiente.
##### También, recuerda estudiar las lecturas designadas para la próxima semana. Puedes revisarlas en "Controles de entrada y lecturas" de la página del curso, [aquí](https://github.com/bioinf-biotec/labs_bioinf). 

---

<p align="center">
<img width="50%" src="https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/unab_cbib_horizontal.png?raw=true">
</p>
