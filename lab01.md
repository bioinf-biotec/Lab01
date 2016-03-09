# Laboratorio 01 - Bases de datos biológicas
-------------------------

#### En este laboratorio vamos a explorar bases de datos biológicas a través de un ejemplo guiado. La idea de este práctico es que uses y te interiorices con la mayor parte de las herramientas que las bases de datos te pueden ofrecer. Sigue las instrucciones y responde las preguntas. tus respuestas van a formar parte de la nota de laboratorio 1.

#### Parte 1: Enfermedades genéticas y genes

- Busca una enfermedad genética humana en alguna base de datos de literatura, i.e., [Pubmed](www.pubmed.com), [Google Scholar] (scholar.google.com), o en bases de datos de enfermedades genéticas, e.g., [OMIM](http://www.omim.org)  
- Describe en no más de 4 lineas la causa y lo que provoca la enfermedad que escogiste  
- ¿Cuál(es) gene(s) han sido relacionados con esta enfermedad?  

##### Ve a la NCBI Gene database ([http://www.ncbi.nlm.nih.gov/gene](http://www.ncbi.nlm.nih.gov/gene)) y busca el gen que está involucrado en la enfermedad seleccionada. Algunos ejemplos pueden ser   

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
		
		Anteriormente encontraste nombres alternativos de tu gen ¿Existen otros reportados por Kegg?¿Cuáles?
		¿En qué rutas metabólicas participa la proteina codificada por tu gen?  
		¿Cuál es el número de identificación de tu gen (entry number)?  
		En general, cada unidad dentro de una base de datos tiene un número o código de identificación único. De esta forma, uno puede exactamente lo que quiere dentro de un oceano de otras cosas ¿En qué otras bases de datos está tu gen presente y cuáles son sus números de acceso?  

La figura más cásica que se puede obtener es el diagrama con una ruta metabólica. Probablemente tu gen está involucrado en más de una. Escoge una y toma un pantallazo para que lo incluyas en tu informe.

![pathway](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/pathway.png) 

#### Parte 3: Descargando secuencias, convirtiendo formatos

Números de acceso
Descargando genes o secuencias cortas
Descargando genomas, acceso a través de FTP
Convertir secuencia en fasta a nexus
#### Parte 4: Buscando artículos científicos en linea
#### Trabajo de laboratorio para la próxima semana

El trabajo de laboratorio para la próxima semana consta de dos partes. La primera parte ya la tienen parcialmente lista. Simplemente tienen que responder las preguntas que aparecen a través de esta guía y

Pubmed
Highwire
Google Scholar
Scopus
Sci-Hub
Libgen.io
uspto
espacenet
inapi
 
