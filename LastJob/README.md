# Tareas a realizar
A la hora de evaluar lo aprendido a lo largo de estas semanas lectivas se plantean una serie de tareas a realizar 
en las que poner en práctica lo aprendido y demostrarse a uno mismo que la potencia del Machine Learning puede ser determinante en proyectos 
de ciberseguridad.

Se plantean dos tareas con enfoque dispar:

1. Realizar la descripción de un caso de uso de Machine Learning en el ámbito de la cyberseguridad.

2. Desarrollar un modelo predictivo siguiendo las pautas aprendidas.

## 1. Diseño de un casos de uso de ML en Ciber Seguridad:

A lo largo del módulo se han ido estudiando distintos métodos y algoritmos útiles en la resolución de distintos problemas de ciberseguridad a partir de datos.
También hemos aprendido la metodología de desarrollo y hemos estudiado las distintas claves que permiten evaluar el éxito del proyecto.

Como expertos en ciberseguridad vuestro rol será fundamental a la hora de establecer las bases, evaluar y realizar el seguimiento de distintas soluciones
de Machine Learning que se puedan plantear como solución ante un problema de seguridad. Vuestro trabajo en muchos de estos proyectos será definir adecuadamente
este documento y aseguraros de que se van cumpliendo las especificaciones haciendo uso del conocimiento adquirido en este módulo.

Por lo tanto el objetivo de la tarea es plantear la definción de un caso de uso que se pudiera presentar como proyecto potencial a realizar con ML en una compañía
siguiendo las intrucciondes descritas en el documento: **Conceptualización_CasosDeUso_BigData_v20.pdf**


## 2. Resolver usando python uno de los siguiente problemas de ML planteados:

### 2.1 El dataset CTU-13. Es un dataset con distintos tipos de tráficos en red: Botnet, Normal y Background traffic.

El objetivo será identificar el tipo de tráfico que está habiendo en base a las variables recogidas y otras que podáis generar.

El conjunto de datos utilizado será el que podéis encontrar en el siguiente link, donde además podemos ver su estructura.

Se evaluará el resultado pero también el trabajo realizado en base a la metodología Data Science.

[Web oficial de la base de datos](https://mcfp.weebly.com/the-ctu-13-dataset-a-labeled-dataset-with-botnet-normal-and-background-traffic.html)

De todos los escenarios posibles se ha determinado trabajar con el **escenario 7** por contener menos datos y se recomenda utilizar los ficheros csv que se adjuntan.
[Fuente final de datos: Escenario 7](https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-48/)

Encontramos varios ficheros, aunque de todos se puede extraer información valiosa, recomendamos utilizar simplemente:
- [capture20110816-2.binetflow.2.format](https://mcfp.felk.cvut.cz/publicDatasets/CTU-Malware-Capture-Botnet-48/capture20110816-2.binetflow.2format)
Fichero csv que contiene información sobre las distintas conexiones con una variable objetivo final en la columna flow que determina el background.
[Enlace a drive](https://drive.google.com/drive/folders/1CLxUKaWomYzdg68wVhq-y0gCbt2F0HD6?usp=sharing)

Nota: por la complejidad del tratamiento y parseado de datos se plantea como alternativa trabajar en el siguiente problema cuyos datos están pretratados.

### 2.2 Detección de malware en Android
En este caso de uso práctico se pretende resolver un problema de detección de malware en dispositivos Android mediante el análisis del tráfico de red que genera el dispositivo mediante el uso de conjuntos de árboles de decisión.

#### Descripción
El sofisticado y avanzado malware de Android es capaz de identificar la presencia del emulador utilizado por el analista de malware y, en respuesta, alterar su comportamiento para evadir la detección. 
Para solucionar este problema, instalamos las aplicaciones de Android en el dispositivo real y capturamos su tráfico de red. 
El conjunto de datos de CICAAGM se captura instalando las aplicaciones de Android en los teléfonos inteligentes reales semiautomatizados. 
El conjunto de datos se genera a partir de 1900 aplicaciones con las siguientes tres categorías:

**1. Adware (250 apps)**
* Airpush: Designed to deliver unsolicited advertisements to the user’s systems for information stealing.
* Dowgin: Designed as an advertisement library that can also steal the user’s information.
* Kemoge: Designed to take over a user’s Android device. This adware is a hybrid of botnet and disguises itself as popular apps via repackaging.
* Mobidash: Designed to display ads and to compromise user’s personal information.
* Shuanet: Similar to Kemoge, Shuanet also is designed to take over a user’s device.

**2. General Malware (150 apps)**
* AVpass: Designed to be distributed in the guise of a Clock app.
* FakeAV: Designed as a scam that tricks user to purchase a full version of the software in order to re-mediate non-existing infections.
* FakeFlash/FakePlayer: Designed as a fake Flash app in order to direct users to a website (after successfully installed).
* GGtracker: Designed for SMS fraud (sends SMS messages to a premium-rate number) and information stealing.
* Penetho: Designed as a fake service (hacktool for Android devices that can be used to crack the WiFi password). The malware is also able to infect the user’s computer via infected email attachment, fake updates, external media and infected documents.

**3. Benign (1500 apps)**
* 2015 GooglePlay market (top free popular and top free new)
* 2016 GooglePlay market (top free popular and top free new)

#### Ficheros de datos
* pcap files – el tráfico de red del malware y benigno (20% malware y 80% benigno)
http://205.174.165.80/CICDataset/CICDDoS2019/Dataset/PCAPs/03-11/PCAP-03-11.zip
* <span style="color:green">.csv files - la lista de características de tráfico de red extraídas generadas por el CICflowmeter </span>
http://205.174.165.80/CICDataset/CICDDoS2019/Dataset/CSVs/CSV-03-11.zip

Se recomienda de nuevo usar csv.

#### Descarga de los ficheros de datos
[Enlace de descarga](https://www.unb.ca/cic/datasets/android-adware.html)
[Enlace de descarga2](http://205.174.165.80/CICDataset/CICAndAdGMal2017/)
[Fichero csv en drive](https://drive.google.com/drive/folders/1K6EXmxPsSYFTKxIOWiQQMlDdABMfDD9u?usp=sharing)

#### Referencias adicionales sobre el conjunto de datos
_Arash Habibi Lashkari, Andi Fitriah A. Kadir, Hugo Gonzalez, Kenneth Fon Mbah and Ali A. Ghorbani, “Towards a Network-Based Framework for Android Malware Detection and Characterization”, In the proceeding of the 15th International Conference on Privacy, Security and Trust, PST, Calgary, Canada, 2017._
