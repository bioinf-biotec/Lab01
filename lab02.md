# Laboratorio 02 - Alineamiento de secuencias
-------------------------

#### En este laboratorio vamos a navegar a través de los procedimientos básicos de cómo colectar secuencias génicas, cómo realizar un alineamiento múltiple, y cómo diseñar partidores para PCR

#### Parte 1: Colectar genes homólogos

Comencemos por ir a NCBI y buscar un gen de interés.

- Ve a la base  de datos de genes de [NCBI](http://www.ncbi.nlm.nih.gov/gene) y busca el gen SRY.  

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/sry_gene.png)

- Los resultados deberían ser familiares ya que se trata de la base de datos que se usó en el práctico anterior. Ahora, navega en esta página y busca genes ortólogos a SRY (pista: Orthologs from Annotation Pipeline)

**Responde:**  
		
		¿Qué función cumple el gen SRY?
		¿Cuántos genes ortólogos están anotados en esa base de datos?

Dentro de esta base de datos vas a encontrar un listado de genes SRY ortólogos en diferentes especies de animales. 

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/orto.png)

- Descarga la secuencia en formato fasta para cada uno de los ortólogos. Para esto, haz clic en cada uno de los vínculos y navega hasta la sección "NCBI Reference Sequences (RefSeq)"
- En esa sección encontrarás un vínculo que te llevará hasta la secuencia nucleótidica del gen SRY para la especie en cuestión (pista: mRNA and Protein(s))   
- Nos interesa la secuencia del mRNA del gen, no la de proteínas ni la del genoma

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/down_sry.png)

- Una vez que haces clic en el vínculo que te lleva al registro del mRNA del gen, haz clic en *FASTA* y simplemente copia y pega la secuencia en el bloc de notas

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/fasta.png)

#### Perfecto! Ahora ya puedes colectar genes SRY homólogos (ortólogos) presentes en diferentes especies. Antes de avanzar a la siguiente sección deberías contar con un archivo de texto en el bloc de notas con todas las secuencias de mRNA homólogas del gen SRY

#### Parte 2: Alineamiento múltiple

Un alineamiento múltiple trata de comparar genes o regiones genéticas homólogas. La suposición es que cada columna en el alineamiento corresponde a una posición que es homóloga entre todas las secuecias que estás comparando.

- Vamos a la página del EMBL-EBI, específicamente a la de "multiple sequence alignment" ([aquí](http://www.ebi.ac.uk/Tools/msa/))
- El EMBL-EBI provee muchos servicios web entre los cuales están los de alineamiento múltiple. 

**Responde:**  
		
		¿Qué es el EMBL-EBI?
		¿Cuántos tipos de alienamiento múltiple se pueden realizar en EMBL-EBI?
		¿Cuál es el programa que ellos ofrecen que funciona mejor para secuencias de proteínas?
		¿Qué otros tipo de herramientas ofrece EMBL-EBI?

- Haz clic en MAFFT   
- Sube tu archivo de bloc de notas con las secuencias de SRY que descargastes

**Responde:**  
		
		¿Cuál es el costo de abrir un gap?
		¿Cuál es el costo de extender un gap?
		
- Haz clic en "Submit"
- Una vez que termine el programa, haz clic en "Result Summary" y luego en Jalview --> Start Jalview

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/mafft.png)

Jalview es un programa que depende de Java y que sirve para inspeccionar interactivamente el alineamiento

**Responde:**  
		
		¿Cuál es la longitud total del alineamiento?

![gene](https://raw.githubusercontent.com/bioinf-biotec/labs_bioinf/master/jalview.png)

- Ahora haz clic en la filogenia (Phylogenetic tree)
- Familiarizate con los códigos que corresponden a tus secuencias. Esos códigos naturalmente corresponden a las especies de animales donde los ortólogos de SRY fueron encontrados   

**Responde:**  
		
		¿Cuál es la especie cuyo gen SRY está más relacionado con el gen SRY de humanos?
		¿Cuál es el más lejano?
		¿Cuál es la especie cuyo gen SRY es más cercana a la del burro?

Un alienamiento de secuencias es un modelo derivado de una observación directa (secuencia de ADN). Uno puede imaginar un alineamiento de secuencias como una **hipótesis de homología** donde uno afirma que cada columna del alineamiento corresponde a una posición homóloga entre las secuencias.

***"All models are wrong, but some are useful"*** [George Box](http://www.tandfonline.com/doi/abs/10.1080/01621459.1976.10480949)

Teniendo en mente el aforismo más conocido en estadística, uno puede crear otro modelo (o alineamiento) a partir de las mismas secuencias.

- Volvamos a la página principal de MAFFT, selecciona tu archivo y haz clic en "More options"
- Vamos a modificar el costo de abrir un gap y de extender un gap.

**Responde:**  
		
		¿Cómo esperas que sea el alineamiento si el costo de abrir un gap aumenta? ¿Y si disminuye?
		¿Cómo esperas que sea el alineamiento si el costo de extender un gap aumenta? ¿Y si disminuye?

- Prueba aumentando el costo de abrir gaps cambiando el valor de 1.53 a 2.0

**Responde:**  
		
		¿Cuál fue el efecto de aumentar el costo de abrir un gap en la longitud total del alineamiento?
		prueba lo mismo pero esta vez disminuyendo al mínimo el costo de extender un gap. Describe cómo cambia el alineamiento



#### Parte 3: Diseño de partidores
#### Trabajo de laboratorio para la próxima semana
