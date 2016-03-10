# Laboratorio 01 - Bases de datos biológicas
-------------------------

#### En este laboratorio vamos a explorar bases de datos biológicas a través de un ejemplo guiado. La idea de este práctico es que uses y te interiorices con la mayor parte de las herramientas que las bases de datos te pueden ofrecer. Sigue las instrucciones y responde las preguntas. tus respuestas van a formar parte de la nota de laboratorio 1.

#### Parte 1: Enfermedades genéticas y genes

- Busca una enfermedad genética humana en alguna base de datos de literatura, i.e., [Pubmed](www.pubmed.com), [Google Scholar] (scholar.google.com), o en bases de datos de enfermedades genéticas, e.g., [OMIM](http://www.omim.org)  
- Describe en no más de 4 lineas la causa y lo que provoca la enfermedad que escogiste  
- ¿Cuál(es) gene(s) han sido relacionados con esta enfermedad?  

##### Ve a la NCBI Gene database ([http://www.ncbi.nlm.nih.gov/gene](http://www.ncbi.nlm.nih.gov/gene)) y busca el gen que está involucrado en la enfermedad seleccionada. Algunos ejemplos pueden ser CFTR, SGCG, IDDM3, HBB. También puedes tratar directamente con el nombre de una enfermedad o condición (e.g., duchenne muscular dystrophy).   

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/gene.png)

La base de datos de genes de NCBI concentra información de distintas fuentes para producir una "ficha" con vínculos con otras bases de datos.

**Responde:**  
		
		¿Tiene nombres alternativos el gen?  
		¿En qué cromosoma está? ¿Cuántos exones tiene? ¿Cuántas isoformas de transcritos?  
		¿Qué tipo de proteina es codificada por este gen? ¿Cuál es su número EC?  
		¿Qué genes están inmediatamente río arriba/abajo?  

De tus conocimientos de genética básica, probablemente ya sabes que un gen puede tener múltiples alelos, y a su vez estos alelos pueden estar asociados a distintos fenotipos, e.g., enfermedades, severidad, etc. Lista cuántas variantes génicas tiene tu gen y a qué tipo de sustituciones corresponden (pista: revisa la sección de Variation en la página de tu gen).

**Responde:**  
		
		¿Cuál es la longitud de tu gen?
		¿Cuántas variantes de tu gen hay descritas y en qué posiciones?  
		¿Las sustituciones corresponden a cambios sinónimos o no sinónimos?  
		¿Existen ortólogos de tu gen en otras especies? ¿Cuántos?  
		¿Y paralógos? ¿Hay pseudogenes? ¿Cuántos?  

#### Parte 2: Rutas y procesos metabólicos

Los genes generalmente codifican proteinas, las cuales a su vez están involucradas en rutas y procesos metabólicos. Existen bases de datos especializadas que compilan información referente a metabolismo. Las más populares son [BioCyc](http://biocyc.org), [REACTOME](http://www.reactome.org), y [Kegg](http://www.kegg.jp). Otras bases de datos agrupan proteinas involucradas en procesos biológicos más gruesos como [Clusters of Orthologous Groups (COGs)](http://www.ncbi.nlm.nih.gov/pubmed/25428365) o [Gene Ontology (GO)](http://geneontology.org). Visita los vínculos a estas páginas y familiarizate con sus funcionalidades (no más de 10 minutos).  
Ahora sigamos terabajando con el gen que escogiste en la parte 1. Una vez en la página principal de Kegg, haz clic en el vínculo Kegg gene. Busca el gen que escogiste en Kegg. Tienes que ingresar el código del organismo (*Homo sapiens* es hsa) y el nombre del gen en minúscula (por ejemplo: gapdh) de forma que para buscar la gliceraldehido-3-fosfato deshidrogenasa deberías ingresar hsa:gapdh.

![kegg](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/kegg.png)

Después de presionar *entry* una nueva ventana se va a abrir donde encontrarás un montón de información. Revisa esta información para responder las siguientes preguntas:

**Responde:**  
		
		Anteriormente encontraste nombres alternativos de tu gen ¿Existen otros reportados por Kegg? ¿Cuáles?
		¿En qué rutas metabólicas participa la proteina codificada por tu gen?  
		¿Cuál es el número de identificación de tu gen (entry number)?  
		En general, cada unidad dentro de una base de datos tiene un número o código de identificación único. De esta forma, uno puede obtener exactamente lo que quiere dentro de un oceano de otras cosas ¿En qué otras bases de datos está tu gen presente y cuáles son sus números de acceso?  

La figura más cásica que se puede obtener es el diagrama con una ruta metabólica. Probablemente tu gen está involucrado en más de una. Escoge una y toma un pantallazo para que lo incluyas en tu informe.

![pathway](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/pathway.png) 

**Responde:**  

		¿En qué otras rutas metabólicas está involucrado tu gen?
		¿Qué significan los cuadros verdes en el diagrama?
		¿Con qué rutas se cruza la ruta metabólica?

Ahora vamos a la página de [Gene Ontology (GO)](http://geneontology.org). Una ontología es un tipo de anotación genómica que teine que ver con atributos de regiones genómicas o de genes. En este sentido, el gen del citocromo c, por ejemplo,  no es parte de GO pero su actividad biológica, i.e., su atributo, si está (oxidoreductasa). Cualquier persona que quiera hacer un experimento de transcriptómica o genómica, secuenciar un genoma de un organismo, etc. debería tener un entendimiento profundo sobre GO. Un buen comienzo es [este artículo](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1003343#s2) en PLOS Computational Biology.

Ahora, desde el website de GO, lee la documentación para poder responder las siguientes preguntas:

**Responde:**  

		¿Cuántos "dominios" forman la anotación GO?
		Ve a "Tools" --> "AmiGO 2" y escribe en la casilla de búsqueda GO:0006096  
		¿A qué corresponde este término y qué información te entrega la página?
		Haz clic en "Graph Views" y examina el gráfico. Anota 10 sub-categorías GO a la cual GO:0006096 pertenece

![go](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/go.png)


#### Parte 3: Descargando secuencias, convirtiendo formatos

De alguna u otra forma, probablemente ya has tenido algún tipo de interacción con NCBI descargando secuencias nucleotídicas o aminoacídicas. En esta sección nos vamos a enfocar en descargar secuencias y sus números de acceso.

Ve a la página de [NCBI](http://www.ncbi.nlm.nih.gov) y selecciona la base de datos de nucleotidos. En la casilla de búsqueda escribe GAPDH y presiona Enter.

**Responde:**  

		¿Cuántos items fueron encontrados? ¿cuántos en animales?
		Probablemente tus resultados fueron una mezcla de fragmentos de genes, regiones codificantes parciales, genes completos, etc. Filtra tus datos por mRNA, animales, RefSeq.
		Haz clic en la entrada para la secuencia de GAPDH de gallina. 
		¿Cuál es la longitud del gen? 
		¿Cuál es la referencia bibliográfica más reciente? 
		¿Cuál es el número de acceso?
		Descarga la secuencia en formato fasta y agrégala a tu informe

![gapdh](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/gapdh.png)

Como nota adicional, la interfaz gráfica de NCBI no es de mucha ayuda cuando tienes que descargar muchas secuencias o genomas completos. En este caso se recomienda usar el portal FTP de NCBI: [ftp.ncbi.nlm.nih.gov](ftp.ncbi.nlm.nih.gov)

Para finalizar esta parte, vamos a convertir la secuencia que bajaste a otro formato. Existen muchos formatos de secuencias porque responden a distintos atributos que sus autores consideraron importantes de registrar y también por razones históricas. Uno de los formatos más usados es el FASTA, sin embargo en filogenética uno súper popular y requerido por muchos programas es el formato NEXUS.

Ve a la página de [Seqret](http://www.ebi.ac.uk/Tools/sfc/emboss_seqret/) del EBI. Luego copia y pega la secuencia de GAPDH en fasta en la casilla.

Adjunta la secuencia en formato nexus a tu informe.

![nexus](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/nexus.png)
#### Parte 4: Buscando artículos científicos en linea

Buscar literatura relativa a un tema científico no tiene que ser tedioso ni complicado. Al contrario, conociendo herramientas dedicadas para esto puede hacerte la vida muy simple.

En general el primer impulso es buscar en los clásicos buscadores directamente. Sin embargo el uso de alertas, tablas de contenido electrónicas, y por sobre todo modificadores de búsquedas en linea hacen que estar actualizado en tu tema de investigación sea algo instántaneo.

- Crea una cuenta gratuita en NCBI y Google Scholar  
- Escoge un área de investigación, e.g., bacterial genomics, human genetics, etc.
- Ahora crea una alerta de búsqueda en NCBI PubMed

##### En tu informe de laboratorio incluye un pantallazo de tu alerta. Si es que recibes una alerta en tu correo electrónico, también puedes adjuntarla en tu informe.

Las páginas de búsqueda clásicas son:

- [Pubmed](http://pubmed.com), [Highwire](http://highwire.stanford.edu/cgi/search), [Google Scholar](https://scholar.google.com), [Scopus](http://www.scopus.com) para artículos científicos  
- [USPTO](http://www.uspto.gov), [ESPACENET](http://www.epo.org/searching-for-patents/technical/espacenet.html), [INAPI](http://www.inapi.cl/portal/institucional/600/w3-propertyvalue-877.html) para patentes. Google Scholar también permite filtrar resultados por patentes  

Ahora vamos a la página de la revista [Nature Genetics](http://www.nature.com/ng/index.html). El obejtivo es configurar una tabla de contenidos electrónica, i.e., que cada vez que la revista publique un número nuevo te llegue la tabla de contenidos de ese número a tu correo electrónico. Puedes encontrar el vínculo en la esquina superior derecha, bajo el *current issue*, E-alert

![ngen](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/ngen.png)

##### En tu informe agrega un pantallazo del correo electrónico de confirmación a la suscripción.

Para finalizar esta parte vamos a prácticar el uso de *operadores de búsqueda en Google Scholar*. Abre una ventana y entra al Google Scholar. Por ejemplo busca Human Microbiome (puedes buscar cualquier otro término).

Ahora usa comillas para realizar tu búsqueda "Human Microbiome"
			
		¿Son los resultados idénticos o no?

El uso de comillas restringe los resultados a resultados donde la frase que buscas aparece de manera exacta.

También puedes usar * para representar una palabra que falta, e.g., "Human Microbiome *"

		¿En qué cambiaron los resultados de la búsqueda?
		
También puedes condicionar tus búsquedas a rangos de números como precios, años, etc. Prueba con 14 inch...17 inch laptops en google.com

		¿Qué encuentras en los resultados? Prueba sin el rango también

Para buscar artículos científicos también es útil restringir los resultados de búsqueda a tipos de archivo. Prueba con "human microbiome" filetype:pdf

		Describe tus resultados

Otro truco útil es usar signos - y +. Por ejemplo trata buscar "PCR amplification" +temperature, y luego "PCR amplification" -temperature

		¿En qué cambian los resultados de la búsqueda?

Finalmente, prueba los operadores Boolean que representan opciones de inclusión. Por ejemplo, trata con Soil OR Human pathogens y luego trata con Soil AND Human  pathogens

		De nuevo, ¿en qué cambian los resultados de la búsqueda?

Puedes seguir practicando tus habilidades para buscar artículos científicos. Los ejemplos de esta sección fueron tomados desde [acá](http://libguides.mit.edu/c.php?g=176061&p=1159432). 

##### No olvides agregar tus respuestas al informe de laboratorio.

#### Trabajo de laboratorio para la próxima semana

El trabajo de laboratorio para la próxima semana consta de dos partes. La primera parte ya la tienes parcialmente lista. Simplemente tienes que responder las preguntas que aparecen a través de esta guía y enviar un informe a tu ayudante con copia a eduardo.castro@unab.cl. Recuerda que si te la juegas y entregas el informe como documento Markdown tendrás 5 décimas adicionales en tu nota. Información sobre cómo escribir documentos Markdown está en la web por ejemplo [aquí](http://cesarhdz.com/articulos/escribir-en-markdown#que-es-markdown) o [aquí en inglés](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).
La segunda parte del trabajo de laboratorio tiene que ver con leer un capítulo de libro y un artículo científico. Estos serán evaluados la próxima clase como parte del primer control de laboratorio.

- El capítulo 2 del libro *Sequence - Evolution - Function: Computational Approaches in Comparative Genomics* que se llama *Evolutionary Concept in Genetics and Genomics*. Puedes acceder al capítulo gratis a través de NCBI --> Bookshelf [aquí](http://www.ncbi.nlm.nih.gov/books/NBK20255/?report=reader).

- El siguiente artículo científico --> [Gabaldón, T., & Koonin, E. V. (2013). *Functional and evolutionary implications of gene orthology*. Nature Reviews Genetics, 14(5), 360-366.](https://github.com/bioinf-biotec/labs_bioinf/raw/master/Gabaldón_2013_Nat%20Rev%20Genet%20copy.pdf)


