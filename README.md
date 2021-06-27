# FMx Backblaze
Permite usar la API de BackBlaze para gestionar ficheros usando ese servicio de almacenamiento en la nube. Guarda los ficheros fuera del servidor de FileMaker, facilitando la migración y permitiendo optimizar los recursos del sistema

## Modo de uso
Abrir el único script que tiene el fichero e introducir vuestras credenciales de Backblaze. Voilà! Hecho.

## Sobre los componentes FMx
Los componentes FMx se caracterizan por cargar las funciones necesarias desde un fichero de texto externo, alojado en un repositorio público de GitHub. Buscan la máxima funcionalidad con el mínimo codigo posible en Filemaker

## FAQs
### Como funciona?
Hay dos ficheros de textos: fields.txt y parser.txt. Al lanzar el script se cargan ambos como variables globales llamadas $$_text y $$_parser respectivamente. Luego establecemos una variable que evalua cada item en el fichero de texto y lo convierte en una variable global. Estas variables pueden ser plantillas o funciones.
Una vez ejecutado este paso lo único que evaluar - cuando es necesario- estas funciones y ejecutar el cURL con la función nativa de Filemaker.
### Que ventajas tiene?
Es casi imposible encontrar integraciones o addons que no agreguen multiples tablas funciones personalizadas, campos y multiples scripts para incorporar una funcionalidad. Esto complica artificialmente la legibilidad de una solución. lo que buscamos es simplificar al máximo lo necesario. En este caso hemos hecho un refactoring de una solución que usaba 5 scripts,400 líneas de código, 2 tablas y 41 campos, y lo hemos reducido a 40 líneas, 1 tabla y 10 campos. Y cumple las premisas básicas de externalizar el código, hacerlo legible y facilitar el uso de cURL escribiéndolo de forma simple, sin necesidad de escapar comillas.


----------------
# FMx Backblaze
Allows you to use the BackBlaze API to manage files using this cloud storage service. Saving files off the FileMaker server makes database migration easier and optimizes system resources
## About FMx components
FMx components load the necessary functions from an external text file, hosted in a public GitHub repository. They look for the maximum functionality with the minimum possible code in Filemaker
## How to use
Open the only script that has the file and enter your Backblaze credentials. Voilà. Done
