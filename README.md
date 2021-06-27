# FMx Backblaze
Permite usar la API de BackBlaze para gestionar ficheros usando ese servicio de almacenamiento en la nube. Guarda los ficheros fuera del servidor de FileMaker, __facilitando la migración__ y permitiendo __optimizar los recursos__ del sistema

## Modo de uso
Abrir el único script que tiene el fichero e introducir vuestras credenciales de Backblaze. Voilà! Hecho.

## Sobre los componentes FMx
Los componentes FMx se caracterizan por cargar las funciones necesarias desde un __fichero de texto externo__, alojado en un repositorio público de GitHub. Buscan la __máxima funcionalidad__ con el mínimo codigo posible en Filemaker

## FAQs
### Como funciona?
Hay dos ficheros de textos: __fields.txt__ y __parser.txt__. Al lanzar el script se cargan ambos como variables globales llamadas __$$_text__ y __$$_parser__ respectivamente. Luego establecemos una variable que __evalua__ cada item en el fichero de texto y lo convierte en una variable global. Estas variables pueden ser __plantillas__ o __funciones__.
Una vez ejecutado este paso lo único que evaluar - cuando es necesario- estas funciones y ejecutar el cURL con la función nativa de Filemaker.
### Que ventajas tiene?
Es casi imposible encontrar integraciones o addons que no agreguen multiples tablas funciones personalizadas, campos y multiples scripts para incorporar una funcionalidad. Esto __complica artificialmente la legibilidad de una solución__. lo que buscamos es __simplificar al máximo__ lo necesario. En este caso hemos hecho un refactoring de una solución que usaba 5 scripts,400 líneas de código, 2 tablas y 41 campos, y lo hemos reducido a __un sólo script__ con 40 líneas, 1 tabla y 10 campos. Y cumple las premisas básicas de __externalizar el código__, hacerlo __legible__ y __facilitar el uso de cURL__ escribiéndolo de forma simple, sin necesidad de escapar comillas.


----------------
# FMx Backblaze
Allows you to use the BackBlaze API to manage files using this cloud storage service. Saving files off the FileMaker server makes database migration easier and optimizes system resources
## About FMx components
FMx components load the necessary functions from an external text file, hosted in a public GitHub repository. They look for the maximum functionality with the minimum possible code in Filemaker
## How to use
Open the only script that has the file and enter your Backblaze credentials. Voilà. Done
