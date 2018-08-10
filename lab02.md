# Laboratorio 02 - Alineamiento de secuencias ![](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/vertical-alignment.png?raw=true)

#### En este laboratorio vamos a navegar a través de los procedimientos básicos de cómo colectar secuencias génicas, cómo realizar un alineamiento múltiple, y cómo diseñar partidores para PCR. Sigue las instrucciones y responde las preguntas, entre `[]` se indica el puntaje asignado a cada pregunta. Tus respuestas van a formar parte de la nota de laboratorio 02.

### Parte 1: Colectar genes homólogos

Comencemos por ir a NCBI y buscar un gen de interés.

- Ve a la base de datos Gene de [NCBI](http://www.ncbi.nlm.nih.gov/gene), escribe "SRY" en la barra de búsqueda y selecciona el gen SRY de _Homo sapiens_ (human).

![gene_sry](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/sry_gene.png?raw=true)

- Los resultados deberían ser familiares, ya que, se trata de la base de datos que se usó en el práctico anterior. Ahora, navega en esta página y busca genes ortólogos a SRY (pista: "Orthologs from Annotation Pipeline").

---  
		
**1.** ¿Qué función cumple el gen SRY? [2]

**2.** ¿Cuántos genes ortólogos están anotados en esa base de datos? [1]

---

Dentro de esta base de datos vas a encontrar un listado de genes SRY ortólogos en diferentes especies de animales. 

![orto_sry](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/sry_ortholog.png?raw=true)

- Descarga la secuencia en formato FASTA para cada uno de los ortólogos. Para esto, haz clic en cada uno de los vínculos y navega hasta la sección "NCBI Reference Sequences (RefSeq)".
- En esa sección encontrarás un vínculo que te llevará hasta la secuencia nucleótidica del gen SRY para la especie en cuestión (pista: "mRNA and Protein(s)").
- **Nos interesa la secuencia del mRNA del gen**, no la de proteínas ni la del genoma.

![sry_mrna](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/sry_mrna.png?raw=true)

- Una vez que haces clic en el vínculo que te lleva al registro del mRNA del gen, haz clic en *FASTA* y simplemente copia y pega la secuencia en un editor de texto (e.g., bloc de notas). Haz esto para cada uno de los ortólogos y tendrás un archivo con todas las secuencias.

![sry_fastas](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/sry_fastas.png?raw=true)

##### Perfecto! Ahora ya puedes colectar genes SRY homólogos (ortólogos) presentes en diferentes especies. Antes de avanzar a la siguiente sección deberías contar con un archivo con todas las secuencias de mRNA homólogas del gen SRY. También puedes copiar las secuencias [acá](https://github.com/bioinf-biotec/labs_bioinf/raw/master/documents/SRY_orthologs_mRNAs.fasta).

### Parte 2: Alineamiento múltiple

Un alineamiento múltiple trata de comparar genes o regiones genéticas homólogas. La suposición es que cada columna en el alineamiento corresponde a una posición que es homóloga entre todas las secuecias que estás comparando.

- Vamos a la página del EMBL-EBI, específicamente a la de [Multiple Sequence Alignment](http://www.ebi.ac.uk/Tools/msa/).
- El EMBL-EBI provee muchos servicios web entre los cuales están los de alineamiento múltiple.

--- 

**3.** ¿Qué es el EMBL-EBI? [2]

**4.** ¿Cuál es el programa que ellos ofrecen que funciona mejor para secuencias de proteínas? [2]

**5.** ¿Qué otros tipo de herramientas ofrece EMBL-EBI? [2]

---

- Haz clic en MAFFT.
- Sube tu archivo de bloc de notas con las secuencias de SRY que descargaste.

---

**6.** ¿Cuál es el costo de abrir un gap? [1]

**7.** ¿Cuál es el costo de extender un gap? [1]

---

- Haz clic en "Submit".
- Una vez que termine el programa, haz clic en "Result Summary" y luego en Jalview --> Start Jalview.

![mafft](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/mafft.png?raw=true)

Jalview es un programa que depende de Java y que sirve para inspeccionar interactivamente el alineamiento

![jalview](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/jalview.png?raw=true)

---
		
**8.** ¿Cuál es la longitud total del alineamiento? [1]

---

- Ahora, haz clic en la filogenia (pestaña: Phylogenetic Tree).
- Familiarizate con los códigos que corresponden a tus secuencias. Esos códigos naturalmente corresponden a las especies de animales donde los ortólogos de SRY fueron encontrados.

---
		
**9.** ¿Cuál es la especie cuyo gen SRY está más relacionado con el gen SRY de humanos? [2]

**10.** ¿Cuál es el más lejano? [2]

**11.** ¿Cuál es la especie cuyo gen SRY es más cercana a la del burro? [2]

---

Un alienamiento de secuencias es un modelo derivado de una observación directa (secuencia de ADN). Uno puede imaginar un alineamiento de secuencias como una **hipótesis de homología** donde uno afirma que cada columna del alineamiento corresponde a una posición homóloga entre las secuencias.

Teniendo en mente el aforismo más conocido en estadística, uno puede crear otro modelo (o alineamiento) a partir de las mismas secuencias.

- Volvamos a la página principal de [MAFFT](https://www.ebi.ac.uk/Tools/msa/mafft/), selecciona tu archivo y haz clic en `More options...`.
- Vamos a modificar el costo de abrir un gap y de extender un gap.

---
		
**12.** ¿Cómo esperas que sea el alineamiento si el costo de abrir un gap aumenta? ¿Y si disminuye? [3]

**13.** ¿Cómo esperas que sea el alineamiento si el costo de extender un gap aumenta? ¿Y si disminuye? [3]

---

- Prueba aumentando el costo de abrir gaps cambiando el valor de 1.53 a 2.0.

---
		
**14.** ¿Cuál fue el efecto de aumentar el costo de abrir un gap en la longitud total del alineamiento? [2]

**15.** Prueba lo mismo, pero esta vez **disminuyendo al mínimo el costo de extender un gap**. Describe cómo cambia el alineamiento. [2]

---

#### Parte 3: Diseño de partidores

Ya llegaste a la última parte de este laboratorio. Aquí vamos a seleccionar la secuencia del gen SRY de _Homo sapiens_ (human).

- Las seceuncias que descargaste anteriormente corresponden a las secuencias de mRNA. Para este ejercicio necesitamos la **seceuncias codificante o Coding Sequence (CDS)**.
- Ve nuevamente a la base de datos Gene de NCBI y busca el gen SRY de humano.
- Dirígete a "NCBI Reference Sequences (RefSeq)", en "_mRNA and Protein(s)_" y haz clic en el número de acceso de la secuencia del mRNA.
- Ahora, en vez de hacer clic directamente en FASTA, baja hasta el vínculo que dice **CDS**.
- Una pequeña ventana va a aparecer, haz clic en *FASTA* y copia esa secuencia en un editor de texto.

##### Perfecto! ya estás listo para diseñar partidores para amplificar el gen SRY. Para hacerlo vamos a utilizar dos herramientas:

##### 1. [Primer3](http://primer3.ut.ee) provee de varias secuencias como posibles partidores. Se utiliza online.

![primer3](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/primer3.png?raw=true)

##### 2. [AmplifX](http://jim.nord.univ-mrs.fr/recherche/equipe-t-brue/jullien-nicolas/programmation/amplifx/?lang=en) es un programa que nos permite hacer un PCR _in silico_, es decir, con AmplifX podemos simular la amplificación del gen probando los diferentes partidores propuestos por Primer3 y escoger la mejor combinación de _forward_ y _reverse_. Dirígete a la página y descarga AmplifX según tu sistema operativo e instala el programa.

![amplifx](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/amplifx.png?raw=true)

- Dirígete a la página de [Primer3](http://primer3.ut.ee) y copia y pega la secuencia codificantes del gen SRY de humano.
- Haz clic en `Pick Primers`.
- Al terminar, verás una página con los partidores propuestos. Tómate unos minutos para mirar los resultados.

![primer3_out](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/primer3_out.png?raw=true)

---

**16.** Agrega a tu informe una lista de los "_LEFT PRIMER_" y "_RIGHT PRIMER_" que obtuviste usando Primer3. [3]

---

- Ahora, vamos a usar AmplifX para hacer una amplificación _in silico_ con todos los partidores propuestos por Primer3.
- Abre AmplifX.
- Primero, en `Sequence` pega la secuencia codificante del gen SRY de _Homo sapiens_. También aumenta `Speed/Sensitivity` al máximo, y define la opción `Amplicon max length` a 1000 bp.

![amplifx1](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/amplifx1.png?raw=true)

- Segundo, en `Primer list` haz clic derecho, selecciona "Add a primer", y copia y pega la secuencia del primer partidor sugerido por Primer3. Repite éste paso para todos los partidores _forward_ y _reverse_ que obtuviste. Asegúrate de recordar cuáles son _forward_ y cuáles son _reverse_. En AmplifX puedes nombrar cada secuencia que vas agregando.
- Selecciona un partidor _forward_ y uno _reverse_ y haz clic en `Run PCR` para hacer tu primer PCR _in silico_.

![amplifx2](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/amplifx2.png?raw=true)

- Haz varios PCRs probando diferentes combinaciones de partidores.
- Si haces clic en el amplicón podrás ver información valiosa acerca de la amplificación. Además, al seleccionar un partidor, en la parte derecha del programa, podrás ver algunas carácteristicas como el porcentaje de GC. Usa esta información para escoger la mejor combinación de partidores para tu PCR.

![amplifx3](https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/amplifx3.png?raw=true)

---

**17.** Indica los partidores _forward_ y _reverse_ que escogiste y explica por qué son la mejor opción para amplificar el gen SRY de humano. [5]

**18.** ¿Cuál es el largo del amplicón? ¿Y la temperatura de _annealing_ sugerida? [3]
	
---

##### No olvides enviar tu informe de laboratorio al correo electrónico de la profesora ayudante: kat.mendez@uandresbello.edu. Tienes plazo hasta las 23:59 hrs del día jueves de la semana siguiente.
##### También, recuerda estudiar las lecturas designadas para la próxima semana. Puedes revisarlas en "Controles de entrada y lecturas" de la página del curso, [aquí](https://github.com/bioinf-biotec/labs_bioinf). 

---

<p align="center">
<img width="50%" src="https://github.com/bioinf-biotec/labs_bioinf/blob/master/images/unab_cbib_horizontal.png?raw=true">
</p>
