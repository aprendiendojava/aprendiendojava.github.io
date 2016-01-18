---
slug: eclipse_portable
---

Monta tu propio Eclipse reutilizable y ligero
===============================================
En el momento de escribir este tutorial las versiones más recientes de 
los programas que vamos a utilizar eran las siguientes:

- [Runtime Platform 
Binary](http://archive.eclipse.org/eclipse/downloads/drops4/R-4.5.1-201509040015/#PlatformRuntime)
- [Java Development 
Kit](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

------------

# Table of content
 - Primero descargaremos una versión mínima de Eclipse.
 - Montaremos un JDK portable que sólo utilizaremos con nuestro Eclipse.
 - Aprenderemos a montar Eclipse autocontenido: de manera que podamos 
transportarlo en una memoria usb, cambiarlo de directorio, compartirlo 
con el resto de miembros de tu equipo, etc.

---

## Introducción

Existen muchas "ediciones" de Eclipse, el objetivo de éstos es el de 
agilizar la puesta en marcha de un nuevo entorno de desarrollo ya que 
suelen venir con toda una serie de plugins, configuraciones y plantillas 
preinstalados, de forma que podremos comenzar a desarrollar un proyecto 
JAVA, C++, PHP... en cuestión de minutos.

Pero esta comodidad viene con un coste: la más que generosa cartera de 
plugins que vamos a estar ejecutando y que probablemente nunca vamos a 
utilizar. Consumiendo memoria, sobrecargando la interfaz y generando 
confusión entre los recién llegados.

---

## Descargas

#### Solución - Eclipse Platform Runtime Binary

> Es una edición mínima de Eclipse sin soporte de serie para ningún 
lenguaje o toolchain que podremos personalizar a nuestro gusto con las 
herramientas justas indispensables para nuestro proyecto. Además, 
hacerlo nos otorgará un mejor entendimiento y control sobre este Entorno 
de Desarrollo Integrado (IDE).

Descargamos Eclipse **Platform Runtime Binary** de [esta 
dirección](http://download.eclipse.org/eclipse/downloads/) y allí 
pincharemos sobre el número de la última versión estable que encontremos 
(debajo de **Latest Release**).

En la nueva página que se nos abre pincharemos sobre **Platform Runtime 
Binary** (lo encontraremos en el menú de la izquierda). Se nos mostrará 
entonces un listado con los enlaces para las direntes arquitecturas y 
plataformas soportadas por Eclipse. Descargamos la que corresponda.

#### Java Development Kit
Compuesto por las librerías y utilidades oficiales de Oracle necesarias 
para la creación de aplicaciones JAVA que se ejecuten en la Máquina 
Virtual Java; el JDK incluye al Java Runtime Environment: los 
componentes mínimos necesarios para poder ejecutar aplicaciones JAVA en 
nuestro equipo.

Podemos descargar la última versión del JDK desde 
[aquí](http://www.oracle.com/technetwork/java/javase/downloads/index.html) 
(asegurarnos de descargar el JDK y no el JRE).

###### JDK - WINDOWS
Los usuarios de Windows, en este caso, no están de suerte. Oracle no 
distribuye versiones portables del JDK para Windows (cosa que sí hace 
para la versión de Linux). Por lo que la forma convencional de 
"conectar" nuestro Eclipse con el JDK será instalar el JDK. Para conocer otro 
métodos que no requieren la instalación del JDK visita la sección 
ECLIPSE PORTABLE más abajo.

###### JDK - LINUX
Oracle ofrece dos descargas alternativas para sistemas Linux: 
paquetes específicos de instalación RPM ó los binarios genéricos 
comprimidos en TAR.GZ.
En nuestro caso preferiremos la descarga en TAR.GZ ya que nos será de 
utilidad para el siguiente paso.

---

## Hazlo portable

Nuestro objetivo es conseguir un Eclipse autocontenido y portable capaz 
de ejecutarse en cualquier sistema, sin requisitos externos de librerias 
o software:

#### Eclipse

Descomprimimos el TAR.GZ en cualquier carpeta de nuestro sistema. 
Debería crearnos una carpeta con el nombre "eclipse". No ejecutamos aún.

#### JDK

El siguiente paso se basa en una característica poco documentada de 
Eclipse. Esto es, al arrancar Eclipse busca dentro de su directorio por 
una carpeta llamada "jre" que contenga un JDK. En caso de encontrarla 
usará dicho JDK por defecto, eliminando la necesidad de tener que 
instalar un JDK en nuestro sistema y permitiendo, por ejemplo, llevar 
Eclipse en una memoria usb, etc.

##### Windows (Alternativa al instalador)

###### Solución rápida

- Copiarnos la carpeta "jdk1.8.0_66"(la numeración dependerá de la 
versión que nos hayamos descargado) de otro Windows en el que hayamos 
instalado el JDK con anterioridad.
- Pegamos la carpeta "jdk1.8.0_66" dentro de la carpeta "eclipse"
- Renombramos nuestra carpeta "jdk1.8.0_66" a "jre"
Renombramos 

###### Solución completa

https://techtavern.wordpress.com/2014/03/25/portable-java-8-sdk-on-windows/

##### Linux

- Descomprimimos el TAR.GZZ en cualquier carpeta de nuestro sistema. 
Debería crearnos una carpeta con un nombre del tipo "jdk1.8.0_66"(la 
numeración dependerá de la versión que nos hayamos descargado)
- Cortamos y pegamos esta carpeta dentro de la carpeta "eclipse" que 
obtuvimos en el paso anterior.
- Renombramos nuestra carpeta "jdk1.8.0_66" a "jre".
