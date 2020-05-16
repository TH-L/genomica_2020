# Comandos de la Práctica 03
## Luis Tenorio Hernández

## Parte 1
1.1 ¿A qué organismo pertenece?
	A *Mycoplasma genitalium* cepa G-37

1.2 ¿Es un gen o una región genómica de importancia?
	Es parte de la secuencia de RNA ribosomal, subunidad 16S 

1.3 ¿Qué es un marcador molecular? 
	Es una región de DNA cuya posición en el genoma puede identificarse. Tiene diferentes funciones,por ejemplo al comparar la misma región en genomas de diferentes organismos se pueden inferir relaciones filogenéticas entre ellos, también pueden ser útiles para identificar especies o incluso se pueden usar para inferir la predisposición a enfermedades al detectar el o los genotipos asociados a una patología

1.4 ¿Cuál es la importancia de este marcador en particular?
	El RNA ribosomal se ha utilizado muy prolificamente para inferir relaciones filogenéticas entre grupos de bacterias, debido a que es una región altamente conservada, en la que a mayor similitud existe una relación evolutiva más cercana.También ha sido muy útil para identificar bacterias tanbto conocidas como desconocidas en muestras ambientales en estudios metagenómicos

2.0 
	| BLAST | Definición  | Aplicación  |
	| ----- | ----------- | ----------- | 
	| blastn | Alinea secuencias de nucleotidos con secuencias de nucleotidos |Se puede usar para alinear regiones de genomas y secuencias de RNA |
	| blastp | Alinea secuencias de aminoácidos con secuencias de aminoácidos |Se puede utilizar para alinear péptidos o partes de péptidos con secuencias lineales en la base de datos de ncbi |
	| blastx | Traduce los codones en la secuencia de nucleotidos, considerando los posibles marcos de lectura, a aminoácidos y los alinea con secuencias de aminoácidos | Se puede utilizar para buscar a que péptidos codifican determinadas secuencias de mRNAs | 
	| tblastn |Dada una secuencia de aminoácidos se convierte en las posibles secuencias de nucleotidos |Se podría usar para conocer que gen codifica para el péptido en cuestión | 

3.0 
	En el artículo ['Clock-dependent chromatin topology modulates circadian transcription and behavior'](http://genesdev.cshlp.org/content/32/5-6/347.long) se analizaron datos de 4C-seq, una estrategia experimental que permite recuperar las interacciones en el espacio tridimensional de una región genómica de interés con el resto del genoma.
	Los autores utilizaron  el software Bowtie2 para mapear archivos en formato fastq obtenidos por un proceso de 'demultiplexing' con el genoma de ratón (mm9), usaron los parámetros preestablecidos por HTSstation.

## Parte 2

1.0 ¿En qué consiste el problema de los puentes de la ciudad de Königsberg? ¿Por qué no tiene solución?
	El problema consiste en cruzar los siete puentes de la ciudad de Königsberg sólo una vez, estos puentes conectan a 2 islas y dos porciones de tierra, separadas por un río.
	Para que tuviera solución debedería cumplir con alguna de las siguientes características: (1)El número de el número de conexiones (en este caso puentes) entre los nodos (las dos islas y las dos porciones de tierra) deben ser todas números pares, o (2)Que existan sólo dos nodos con un número de conexiones impar, además uno de los nodos debe ser el inicio de la ruta y el otro el final.
	El problema de los puentes de la ciudad de Königsberg consta de 4 nodos pero todos ellos con un número impar de puentes, por lo cual no tiene solución.

2.0 Tres problemáticas comunes en la aplicación de las gráficas de Bruijin a genomas:
	1.- Las lecturas obtenidas por técnicas de secuaciacion de alto rendimiento generalmente son del orden de 100 pares de bases sin embargo no representan la mayoría de los 100-meros presentes en el genoma por lo que la estrategia a seguir es "romper" esos 100-meros en k-meros más pequeños.
	2.- Existe la probabilidad de que determinadas secuencias est[en repetidas en diferentes regiones del genoma y no es posible tener esta información a priori, las modalidades de secuenciación pareada y herramientas computacionales han ayudado a lidiar con esta problemática.
	3.- Las lecturas obtenidas a través de la secuenciación pueden tener errores que dificultan el ensamble usando métodos de gráficas de Bruijin. Para solucionar este problema se han generado algoritmos y softwares.

3.0 ¿Qué son?, ¿en qué consisten? y ¿para qué se usan? las estadísticas N50 y L50.
	El estadístico N50 es un indicador cuantitativo de la calidad del ensamblaje, es decir, de que tan efectivo fue el programa en unir las secuencias en una única secuencia. El estadístico está definido como la longitud de contig mínima necesaria para cubrir la mitad del genoma. Esto significa que la mitad de las secuencias del genoma está en contigs mayores o iguales a N50.
	Mientras que el estadístico N50 describe la longitud de los contigs, el estadístico L50 describe el número de de los mismos. Se define como el número de contigs evaluados al punto que exceden el 50 % del tamaño del ensamble.

