# Laboratorio 03 - Ensamblaje de genomas y predicción de genes
-------------------------

#### En este laboratorio vamos a familiarizarnos con publicaciones de genomas, y como estos genomas fueron ensamblados. También vamos a explorar dos métodos de predicción de genes

#### Parte 1: El artículo genoma

Hasta hace un tiempo, secuenciar un genoma te garantizaba una publicación importante y era considerado un hito en el estudio de alguna especie. Hoy en día, con los costos decrecientes asociados a un proyecto genoma, publicar un genoma ya no es algo exclusivo sino más bien se está volviendo rutinario en la práctica de un investigador. Comencemos por ir a la Genomes on Line Database (GOLD) y escoger un genoma de interés

- Ve a la base  de datos [GOLD](https://gold.jgi.doe.gov) y busca un genoma eucarionte de interés.  

![gold](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/gold.png)

- Navega dentro del portal siguiendo vínculos a, por ejemplo, "Complete projects", "Eukarya" o la casilla de búsqueda.

**Responde:**  
		
		¿Cuántos genomas han sido depositados en GOLD? ¿Son los mismos de GENBANK?
		¿Cuál es la distribución de procariontes y eucariontes secuenciados?

En este ejemplo continuaremos con el genoma del Bonobo *Pan paniscus*

![pan](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/pan.png)

- A partir de la ficha GOLD de tu organismo, busca la publicación de su genoma (pista: sigue el Taxonomy ID)
- Busca el vínculo a la base de datos de genomas de NCBI y ubica la referencia al artículo original

![pangeno](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/pangeno.png)

- Ahora solo tienes que conseguir el artículo y buscar en los materiales y métodos para responder las siguientes proguntas. Existen una serie de métricas o estadísticas que se usan para evaluar un ensamblaje de genomas.
- Sigue [este vínculo](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics) y revisa las siguientes N50, L50, y NG50.

![panstats](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/panstats.png)

**Responde:**  
		
		¿Qué es el N50, L50, NG50?
		¿Cuál es el propósito de calcular estas estadísticas?
		¿Cuál es el genoma que escogiste? Adjunta la referencia.
		¿Cuál es el N50 del genoma que escogiste? ¿Y el NG50?
		¿Qué tipo de tecnología se uso para secuenciar el genoma que escogiste?
		¿Qué organismo escogiste, cuántos cromosomas tiene tu organismo y cuál es su tamaño?


#### Parte 2: Predicción de genes

En esta parte vamos a utilizar dos programas clásicos para predecir genes [ORFfinder](http://www.ncbi.nlm.nih.gov/gorf/gorf.html) y [GLIMMER](http://www.ncbi.nlm.nih.gov/genomes/MICROBES/glimmer_3.cgi).  

-  Tu misión para esta parte es descargar una secuencia y predecir qué genes están presentes usando ambas herramientas.    
-  Descarga la secuencia problema [aquí](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/secuencia.fasta) o copia y pega desde:

		ATGAGTATCAAAATCTTATCTGAATCAGAAATTAAACAAGTAGCAAATTCATATCAAGCCCCAGCGGTTTTATTTGCCAATCCTAAAAATCTTTACCAACGCAGAGCGAAACGTTTAAGAGACTTAGCACAAAATCATCCTCTATCTGATTATTTATTATTTGCTGCAGACATAGTTGAAAGCCAACTTTCCACGTTAGAAAAAAATCCTTTACCGCCACAACAGCTTGAACAGTTAAATACTATCGAGCCACTAAATGCCAAAACCTTTAAGAGAAACAGTATCTGGCGTGAATACTTAACAGAAATTCTTGATGAAATAAAGCCCAAAGCTAACGAGCAAATTGCTGCAACAATTGAATTTCTTGAAAAAGCCTCTTCCGCTGAATTAGAAGAAATGGCAAATAAACTCTTAGCACAAGAATTTAACTTAGTCAGCAGTGATAAAGCCGTCTTTATTTGGGCTGCACTTTCCCTTTATTGGTTACAAGCAGCTCAACAAATTCCTCATAATAGCCAAGTTGAAAACGCTGAAAATTTACATCACTGCCCTGTTTGTGGTTCTTTACCTGTGGCAAGTATGGTACAAATTGGTACATCACAAGGTTTACGCTACTTACATTGTAATTTATGTGAAAGTGAATGGAATTTGGTACGCGCACAATGCACCAATTGTAATAGTCATGACAAACTCGAAATGTGGTCACTAAATGAAGAACTTGCGCTTGTTCGTGCCGAAACCTGTGGTAGTTGTGAAAGTTACTTGAAAATGATGTTCCAAGAAAAAGATCCTTACGTAGAACCTGTAGCCGATGATTTGGCTTCTATTTTCTTAGATATTGAAATGGAAGAAAAAGGTTTCGCCCGAAGTGGATTAAATCCATTTATTTTTCCTGCAGAAGAAGCATAAAAATATAGCCTAGAAATATCTAGGCTAATTATTTAAATCTATAGATAACACGCCATTACCACTGCATTTTCTCGTCCACCACTGGGTTTCGGATAATAATTTTTCCGAATATCCACTTCATTAAAACCAATTTTTTCATACAAGAAACGAGCAGAGTTAGACTCTCTGACTTCTAGCCATAAGGTTTGGACACCTTTTTCCTTTAATTGAAAGATTAATTTTCCTAACAATAATTTGCCAAATCCACAACCTTGATAAGTAGGCAAAATCGCAATATTAAACAAAGTCGCTTCATCCAATACTGTTTGGCAAATAGCAAAACCGATAATCTGATTATTCTCTATTAATTTTAAATTGAGATAACGCTCCCCTTGATTATTTTTTAACGTACCAAATGACCAAGGCACCAGATGGGCTTGCTGTTCGATTTCATACAATCGCTCGAAATCACAGGCTTCAATTTGAGAAATAATAGACATAATTAAGGCTGCTGAATTTGTTGCCACAACGCTCGTTTGGCTTGATGATTAGATTGAAATTGCTGCCAACTTGGCGAGCGATAAACCTGCTCAGCCTGCTTGCAAAATGGCAAAGTGCGGTCAATTTGGTCGCTATTTTCTGATAGTAACCAATAACGAATAGGCTGTTTACATTCCATATGCTGGATTTGATCGTAATTCAAACATAAACAATTTTCTTTTTTAAGATTAAGGCTTAACAGCACATCAGCCAACAAAGGCGAGCTACTGATATTTTCATCGGAAACAGTGATAAGGCGAATATTCTCTGCCACACTAATTCCTACTGAACCTTGCAGTACCTCGGGGCGATATAATTCCCACTGGGAAATGCCCATTTCTTGTAAAAGAAGATCGCGTCTGTTCATAAGTGAATTTTTAAAAACGTTGCTTGAAAAATAGTGTTAATTTCTTTTATTAATCTTTGCTAAAATGGTGCGTAATTTTAACCAATAACCCACAGGATTCAAAGCG

**Responde:**  
		
		¿Cuántos ORF o genes encontró ORFfinder?
		¿Cuántos ORF o genes encontró Glimmer?
		¿Alguno de los genes predichos por estas herramientas coinciden?
		¿En qué hebra están codificados?
		¿Qué tipo de programa es GLIMMER? ¿Ab initio o por homología?
Finalmente realiza una búsqueda en [BLAST](http://blast.ncbi.nlm.nih.gov/Blast.cgi) para confirmar que los genes que has predicho existan en GENBANK. 
	
		Describe los resultados encontrados con respecto a los genes que encontraste con GLIMMER y ORFfinder

#### Trabajo de laboratorio para la próxima semana

El trabajo de laboratorio para la próxima semana, como siempre, consta de dos partes. La primera parte ya la tienes lista. Simplemente tienes que responder las preguntas que aparecen a través de esta guía y enviar un informe (ojalá en MarkDown) a <bit120.unab.republica@gmail.com>. Envien a este correo los informes hasta el jueves de la semana siguiente a la realización del práctico. La hora límite es las 23:59.  
En el Asunto del correo pongan Informe de Laboratorio 0x así nosotros podemos clasificar automáticamente los informes. Para la próxima semana el Asunto del correo debería ser Informe de Laboratorio 03.

La segunda parte tiene que ver con leer un artículo científico sobre este tema: Mihai Pop. 2013. *Sequence assembly demystified*. **Nature Reviews Genetics** 14, 157-167 | doi:10.1038/nrg3367.   

Puedes acceder al artículo [aquí](https://github.com/bioinf-biotec/labs_bioinf/raw/master/pop.pdf). Recuerda que el contenido de este artículo es el material para el próximo control de entrada.


