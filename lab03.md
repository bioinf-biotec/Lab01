# Laboratorio 03 - Ensamblaje de genomas y predicción de genes ![](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/puzzle.png?raw=true)

#### En este laboratorio vamos a familiarizarnos con publicaciones de genomas, y cómo estos genomas fueron ensamblados. También vamos a explorar dos métodos de predicción de genes. Sigue las instrucciones y responde las preguntas, entre `[]` se indica el puntaje asignado a cada pregunta. Tus respuestas van a formar parte de la nota de laboratorio 03.

### Parte 1: El artículo genoma

Hasta hace un tiempo, secuenciar un genoma te garantizaba una publicación importante y era considerado un hito en el estudio de alguna especie. Hoy en día, con los costos decrecientes asociados a un proyecto genoma, publicar un genoma ya no es algo exclusivo sino más bien se está volviendo rutinario en la práctica de un investigador.

- Comencemos por ir a **[_Genomes On Line Database_ (GOLD)](https://gold.jgi.doe.gov)**. GOLD es una base de datos de proyectos de secuenciación de genomas y metagenomas.

![gold](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/gold.png?raw=true)

- Tómate unos minutos para navegar dentro del portal. Sigue vínculos a, por ejemplo, "_Distribution Graphs_" o "_Statistics_".

---

**1.** ¿Cuántos _Sequencing Projects_ y _Analysis Projects_ hay depositados en GOLD? ¿Cuál es la diferencia entre ambos? [2]

**2.** ¿Cuál es el dominio más representado en la base de datos, _archea_, _bacteria_, _eukaryote_, o _virus_? [1]

**3.** ¿Cuáles son los _phyla_ más representados entre los proyectos de genomas bacterianos en la base de datos? [1]

**4.** ¿A qué tipo de proyectos pertenece la mayor cantidad de genomas bacterianos depositados en GOLD? (tipo de proyecto, se refiere al tópico de la investigación, por ejemplo, salud humana, ambiental, etc.) [1]

---

A continuación, vamos a trabajar con el genoma del Bonobo (_Pan paniscus_).

- Ahora, en la página principal de GOLD, dirígete a "_Search_" -> "_Advanced Search_", selecciona "_+ Organism Fields_", luego en "_Domain_" selecciona "EUKARYAL" y en la barra de búsqueda ("_Organism Name_") escribe "_Pan paniscus_" (Bonobo). Haz clic en `Submit Search`.
- Sigue el vínculo a "_Organisms_", y luego al "_GOLD Organism ID_" (Go0003239).

![pan](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/pan.png?raw=true)

- A partir de la ficha GOLD de tu organismo, busca la publicación de su genoma. Pista: sigue el _NCBI Taxonomy ID_.
- Una vez en el _Taxonomy Browser_ de NCBI, verás que en la parte derecha de la pantalla aparece una tabla con links de accesos a información del organismo en diferentes bases de datos. Dirígete al vínculo de la base de datos de genomas.

![pangeno](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/pangeno.png?raw=true)

- Tómate unos minutos para explorar la página y familiarizarte con la información que ofrece.
- Muchos de los genomas depositados en las bases de datos, han sido material de análisis de varios artículos científicos. Ubica la referencia al artículo original del genoma del Bonobo (en el cual se reporta la sequenciación y ensamble del genoma).

Existen una serie de métricas o estadísticas que se usan para evaluar un ensamblaje de genomas. Sigue [este vínculo](https://en.wikipedia.org/wiki/N50,_L50,_and_related_statistics) y estudia las definiciones de **N50**, **L50**, y **NG50**.

![panstats](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/panstats.png?raw=true)

---  

**5.** ¿Cuál es el artículo original del genoma? (en el cual se reporta la sequenciación y ensamble del genoma) [2]

**6.** Explica, qué es el N50, L50, y NG50. [3]

**7.** ¿Cuál es el propósito de calcular estas estadísticas? [3]

**8.** ¿Cuántos _contigs_ conforman el genoma del Bonobo? ¿Cuál es el N50 y L50 del genoma? (responde basado en los _contigs_) [3]

**9.** ¿Cuál es el largo total y porcentaje de GC del genoma del Bonobo? ¿Qué quieren decir o qué indican éstos valores?

**10.** ¿Qué tipo de tecnología se uso para secuenciar el genoma del Bonobo? ¿Qué método (programa o algorítmo bioinformático) se usó para ensamblar el genoma?

---

### Parte 2: Predicción de genes

En esta parte vamos a utilizar un programa clásico para predecir genes **[ORFfinder](https://www.ncbi.nlm.nih.gov/orffinder/)**.

![orffinder](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/orffinder.png?raw=true)

-  Tienes misión es predecir qué gene(s) está(n) codificado(s) en la secuencia a continuación.
		
		ATGAGTATCAAAATCTTATCTGAATCAGAAATTAAACAAGTAGCAAATTCATATCAAGCCCCAGCGGTTTTATTTGCCAATCCTAAAAATCTTTACCAACGCAGAGCGAAACGTTTAAGAGACTTAGCACAAAATCATCCTCTATCTGATTATTTATTATTTGCTGCAGACATAGTTGAAAGCCAACTTTCCACGTTAGAAAAAAATCCTTTACCGCCACAACAGCTTGAACAGTTAAATACTATCGAGCCACTAAATGCCAAAACCTTTAAGAGAAACAGTATCTGGCGTGAATACTTAACAGAAATTCTTGATGAAATAAAGCCCAAAGCTAACGAGCAAATTGCTGCAACAATTGAATTTCTTGAAAAAGCCTCTTCCGCTGAATTAGAAGAAATGGCAAATAAACTCTTAGCACAAGAATTTAACTTAGTCAGCAGTGATAAAGCCGTCTTTATTTGGGCTGCACTTTCCCTTTATTGGTTACAAGCAGCTCAACAAATTCCTCATAATAGCCAAGTTGAAAACGCTGAAAATTTACATCACTGCCCTGTTTGTGGTTCTTTACCTGTGGCAAGTATGGTACAAATTGGTACATCACAAGGTTTACGCTACTTACATTGTAATTTATGTGAAAGTGAATGGAATTTGGTACGCGCACAATGCACCAATTGTAATAGTCATGACAAACTCGAAATGTGGTCACTAAATGAAGAACTTGCGCTTGTTCGTGCCGAAACCTGTGGTAGTTGTGAAAGTTACTTGAAAATGATGTTCCAAGAAAAAGATCCTTACGTAGAACCTGTAGCCGATGATTTGGCTTCTATTTTCTTAGATATTGAAATGGAAGAAAAAGGTTTCGCCCGAAGTGGATTAAATCCATTTATTTTTCCTGCAGAAGAAGCATAAAAATATAGCCTAGAAATATCTAGGCTAATTATTTAAATCTATAGATAACACGCCATTACCACTGCATTTTCTCGTCCACCACTGGGTTTCGGATAATAATTTTTCCGAATATCCACTTCATTAAAACCAATTTTTTCATACAAGAAACGAGCAGAGTTAGACTCTCTGACTTCTAGCCATAAGGTTTGGACACCTTTTTCCTTTAATTGAAAGATTAATTTTCCTAACAATAATTTGCCAAATCCACAACCTTGATAAGTAGGCAAAATCGCAATATTAAACAAAGTCGCTTCATCCAATACTGTTTGGCAAATAGCAAAACCGATAATCTGATTATTCTCTATTAATTTTAAATTGAGATAACGCTCCCCTTGATTATTTTTTAACGTACCAAATGACCAAGGCACCAGATGGGCTTGCTGTTCGATTTCATACAATCGCTCGAAATCACAGGCTTCAATTTGAGAAATAATAGACATAATTAAGGCTGCTGAATTTGTTGCCACAACGCTCGTTTGGCTTGATGATTAGATTGAAATTGCTGCCAACTTGGCGAGCGATAAACCTGCTCAGCCTGCTTGCAAAATGGCAAAGTGCGGTCAATTTGGTCGCTATTTTCTGATAGTAACCAATAACGAATAGGCTGTTTACATTCCATATGCTGGATTTGATCGTAATTCAAACATAAACAATTTTCTTTTTTAAGATTAAGGCTTAACAGCACATCAGCCAACAAAGGCGAGCTACTGATATTTTCATCGGAAACAGTGATAAGGCGAATATTCTCTGCCACACTAATTCCTACTGAACCTTGCAGTACCTCGGGGCGATATAATTCCCACTGGGAAATGCCCATTTCTTGTAAAAGAAGATCGCGTCTGTTCATAAGTGAATTTTTAAAAACGTTGCTTGAAAAATAGTGTTAATTTCTTTTATTAATCTTTGCTAAAATGGTGCGTAATTTTAACCAATAACCCACAGGATTCAAAGCG

---

**11.** Describe los resultados obtenidos. ¿Cuántos ORFs o genes encontró ORFfinder? ¿En qué hebra están codificados? ¿De qué largo son los ORFs predichos? ¿Algunos de ellos se sobreponen (fíjate en la posición de inicio [_start_] y término [_stop_])? [3]

**12.** ¿Qué tipo de programa es ORFfinder, _Ab initio_ o por homología? [2]

---

Finalmente, vamos a utilizar **[BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)** para hacer una búsqueda de la secuencia completa y de cada uno de los ORFs predichos por ORFfinder.

![blast](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/blast.png?raw=true)

- Primero, usa **blastn** (_Nucleotide BLAST_) para consultar la secuencia completa.
- Segundo, usa **blastx** (_translated nucleotide > protein_) para consultar cada uno de los ORFs predichos.

---

**13.** ¿A qué organismo pertenece la secuencia en cuestión? [2]

**14.** ¿Qué gen(s) está(n) codificados en la secuencia? [2]

**15.** Tomando en cuenta la evidencia que acumulaste usando ORFfinder y BLAST. ¿Cuál o cuáles ORFs predichos por ORFfinder dirías tú que son o es el correcto(s)? [3]

---

##### No olvides enviar tu informe de laboratorio al correo electrónico de la profesora ayudante: kat.mendez@uandresbello.edu. Tienes plazo hasta las 23:59 hrs del día jueves de la semana siguiente.
##### También, recuerda estudiar las lecturas designadas para la próxima semana. Puedes revisarlas en "Controles de entrada y lecturas" de la página del curso, [aquí](https://github.com/bioinf-biotec/labs_bioinf). 

---

<p align="center">
<img width="50%" src="https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/unab_cbib_horizontal.png?raw=true">
</p>
