# Solución Tareas a realizar

Se plantean dos tareas con enfoque dispar:

1. Realizar la descripción de un caso de uso de Machine Learning en el ámbito de la cyberseguridad.
En clase hemos visto distintos casos de uso de ciberseguridad tanto de manera completamente aplicada como en su descripción.
En el documento TrabajoML teneís un caso de uso que basándonos en técnicas de hacking intentan buscar una solución basada en tecnología
para un problema cotidiano como es la situación de vulnerabilidad y seguridad de las personas mayores que viven solas, algo que además 
ha tenido gran repercusión en los últimos meses debido al COVID.

Este ejemplo os debe ayudar a:
- Primero identificar todos los factores a tener en cuenta a la hora de definir un caso de uso.
- Segundo a identificar lo aprendido a lo largo del bootcamp como herramientas que deben ser de utilidad para abordar soluciones basadas en datos que partan
del tratamiento de la información que se da en el ámbito de la ciberseguridad a otros.

2. Desarrollar un modelo predictivo siguiendo las pautas aprendidas.

Hemos visto varios casos de uso y las aplicación de modelos que deben servir de referencia.
En este caso la tarea más hardua era trabajar con los datos y convertirlos en tablas organizadas para poder luego aplicar estas técnicas.
Para ello es necesario entender bien el problema, cuales son las entidades de estudio y el objetivo sobre ellas, para posteriormente indagar en referencias del ámbito que hablen de factores
a tener en cuenta a la hora de identificarlos y tratar de representarlos en variables.
 
La pista que el Domingo ya les proporcioné justo con los [datos tratados](https://drive.google.com/file/d/1gagy5UXmCfDQTPxO2MYRt7en5zqK0USy/view?usp=sharing).
En este enlace puende encontrar las tablas que son necesarias para realizar ambos, 2.1  y 2.2

para que pudieran aplicar los distintos modelos fue:



## 2. Resolver usando python uno de los siguiente problemas de ML planteados:

### 2.1 El dataset CTU-13. Es un dataset con distintos tipos de tráficos en red: Botnet, Normal y Background traffic.

Estas son algunas referencias que hablan del problema donde podéis ver distintas perspectivas de construcción de variables y modelado.

* [Web oficial de la base de datos](https://mcfp.weebly.com/the-ctu-13-dataset-a-labeled-dataset-with-botnet-normal-and-background-traffic.html)

* [Paper sobre técnicas de modelado](https://www.scirp.org/html/10-1730818_85035.htm)
	Puntos claves:
	- Se recomienda utilizar F1-Score y MCC, Matthews Correlation Coefficiente, también disponible en skitlear.
* [Paper con solución basada en Redes Neuronales](https://www.diva-portal.org/smash/get/diva2:1352441/FULLTEXT01.pdf)
	- Usa word2vec
* [Paper revisión de distintos métodos de detección no todos ML](https://onlinelibrary.wiley.com/doi/full/10.1002/sec.800)
* [Paper donde se evaluan técnicas de Machine Learning sobre el problema](https://scholarworks.sjsu.edu/cgi/viewcontent.cgi?article=1917&context=etd_projects)
	- Aplicación de label and one-hot encoding
	- Selección de variables:
		* Eliminación de columnas nulas
		* Eliminación de columnas de baja varianza
		* Usando RandomForest
		* Métodos de selección wrapper (vistos en clase)
		* Por importancia de variables
	- Solución al problema de desbalanceo de datos:
		* Undersampling
		* Oversampling
		* Cost-sensitive: usando matrices de costes

Pueden encontrar parte del desarrollo realizado en este [documento](https://github.com/hmishra2250/Botnet-Detection-using-Machine-Learning)

Se adjunta el código para generar el dataset con el que trabajar.
Además se adjunta el código necesario para ejecutar otra solución alternativa con el dataset procesado. 

### 2.2 Detección de malware en Android
En este caso de uso práctico se pretende resolver un problema de detección de malware en dispositivos Android mediante el análisis del tráfico de red que genera el dispositivo mediante el uso de conjuntos de árboles de decisión.

#### Solución
Este caso había sido resuelto en clase, la intención era de nuevo generar un dataset alternativo y trabajar con él con distintos algoritmos.
Las referencias a utilizar son para este nuevo procesado son:
* [Referencia de dato](https://ieeexplore.ieee.org/document/8476939)
* [Trabajo de investigación asociado](https://www.researchgate.net/publication/326991554_CICFlowmeter-V40_formerly_known_as_ISCXFlowMeter_is_a_network_traffic_Bi-flow_generator_and_analyser_for_anomaly_detection_httpsgithubcomISCXCICFlowMeter)
Estas transformadas se realizan usando el siguiente paquete y con los datos originales como fuente [Paquete de generación de features](https://github.com/ahlashkari/CICFlowMeter)

Se adjunta notebook con solución completa sobre el dataset procesado usando estas herramientas.
