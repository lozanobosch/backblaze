# FMx Backblaze
Permite usar la API de BackBlaze para gestionar ficheros usando ese servicio de almacenamiento en la nube. Guarda los ficheros fuera del servidor de FileMaker, __facilitando la migración__ y permitiendo __optimizar los recursos__ del sistema

## Modo de uso
Abrir el único script que tiene el fichero e introducir vuestras credenciales de Backblaze. Voilà! Hecho.

## Sobre los componentes FMx
Los componentes FMx se caracterizan por cargar las funciones necesarias desde un __fichero de texto externo__, alojado en un repositorio público de GitHub. Buscan la __máxima funcionalidad__ con el mínimo codigo posible en Filemaker

## FAQs
### Como funciona?
Hay dos ficheros de textos: __fields.txt__ y __parser.txt__. Al ejecutar el script se cargan ambos como variables globales llamadas **$$_text** y **$$_parser** respectivamente. Luego establecemos una variable que __evalua__ cada item en el fichero de texto y lo convierte en una variable global. Estas variables pueden ser __plantillas__ o __funciones__.
Una vez ejecutado este paso lo único que hacemos es evaluar - cuando es necesario- estas funciones y ejecutar el cURL con la función nativa de Filemaker.
El botón **upload** tiene **dos parámetros**: el primero es la función a ejecutar y el segundo fuerza de nuevo la autentificación si tiene algún valor. El botón **download** agrega a los parámetros del botón de upload, **dos adicionales**: el primero con el id y el segundo con el nombre.
### Que ventajas tiene?
Es casi imposible encontrar integraciones o addons que no agreguen multiples tablas funciones personalizadas, campos y multiples scripts para incorporar cualquier funcionalidad, ya sea integrar una API o una solución que use el web viewer. Esto __complica artificialmente la legibilidad de una solución__. lo que buscamos es __simplificar al máximo__ lo necesario. En este caso hemos hecho un refactoring de una solución que usaba 5 scripts,400 líneas de código, 2 tablas y 41 campos, y lo hemos reducido a __un sólo script__ con 40 líneas, 1 tabla y 10 campos. Y cumple las premisas básicas de __externalizar el código__, hacerlo __legible__ y __facilitar el uso de cURL__ escribiéndolo de forma simple, sin necesidad de escapar comillas.

----------------
# FMx Backblaze
Allows you to use the BackBlaze API to manage files using this cloud storage service. Saving files off the FileMaker server makes database migration easier and optimizes system resources
## About FMx components
FMx components load the necessary functions from an external text file, hosted in a public GitHub repository. They look for the maximum functionality with the minimum possible code in Filemaker
## How to use
Open the only script that has the file and enter your Backblaze credentials. Voilà. Done

## FAQs
### How does it work?
There are two text files: __fields.txt__ and __parser.txt__. When executing the script, both are loaded as global variables called **$$ _text** and **$$__parser** respectively. Then we set a variable that __evalues__ each item in the text file and turns it into a global variable. These variables can be __templates__ or __functions__.
Once this step is executed, all we do is evaluate - when necessary - these functions and execute the cURL with the native Filemaker function.
The ** upload ** button has **two parameters**: the first is the function to be executed and the second forces authentication again if they have any value. The **download** button adds **two additional** to the upload button parameters: the first with the id and the second with the name.
### What advantages does it have?
It is almost impossible to find integrations or addons that do not add multiple tables, custom functions, fields, and multiple scripts to incorporate any functionality. This __artificially complicates the readability of a solution__. what we seek is to __simplify as much as possible__ what is necessary. In this case we have done a refactoring of a solution that used 5 scripts, 400 lines of code, 2 tables and 41 fields, and we have reduced it to __one single script__ with 40 lines, 1 table and 10 fields. And it fulfills the basic premises of __externalizing the code__, making it __legible__ and __ making it easier to use cURL__ by writing it in a simple way, without the need to escape quotes.
