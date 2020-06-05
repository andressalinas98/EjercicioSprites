# APLICACIÓN DE PATRONES CREACIONALES :hammer: :octocat:


La idea principal del proyecto es gestionar un tablero de presentación de personajes de un juego, los cuales se podran ver desde diferentes perspectivas tanto laterales, como el frente, de espaldas y adicionalmente una acción a realizar, para el desarrollo de este programa se debe poner en practica dos patrones creacionales: Builder y Abstract Factory, empleandolos en la creación como tal del personaje.

## DIAGRAMA DE CLASES DEL PROYECTO

![Diagramauml](https://github.com/andressalinas98/EjercicioSprites/blob/master/imagenes/diagrama.jpg)

## ¿Qué son los Patrones Creacionales? :triangular_ruler:

Los patrones de creación abstraen la forma en la que se crean los objetos, permitiendo tratar las clases a crear de forma genérica dejando para más tarde la decisión de qué clases crear o cómo crearlas.

Abstraen el proceso de instanciación, encapsulan conocimiento sobre qué clases concretas utiliza el sistema, independizan al sistema del modo en que se crean, componen y representan los objetos, flexibilizan el qué, quién, cómo y cuándo.

## Abstract Factory :factory:

### ¿Qué es Abstract Factory?
Es un patrón de creación que provee una interfaz para crear familias o conjuntos de objetos(productos) relacionados o que dependen entre sí, sin especificar sus clases concretas.

### ¿Como se implemento?

En el proyecto se puede evidenciar el uso de este patrón cuando creamos los productos que contienen la vista de cada personaje(frente, atras, derecha e izquierda) que en este caso seran las imagenes del sprite,  estos los tomara la fabrica del personaje y los unira para el proceso de creación del mismo genrando asi la fabrica de cada personaje con sus vistas respectivas.

## Builder  :clapper: :construction_worker:

### ¿Qué es Builder? 
Patrón creacional que permite la creación de un objeto complejo, a partir de una variedad de partes que contribuyen individualmente a la creación y ensamblación del objeto mencionado. Hace uso de la frase "divide y conquistarás". Por otro lado, centraliza el proceso de creación en un único punto, de tal forma que el mismo proceso de construcción pueda crear representaciones diferentes.

### ¿Como se implemento?
Para este caso tendremos clases constructores de cada personaje los cuales tendran relación directa con la fabrica respectiva quienes entregaran las partes para su construcción, tendremos una clase director que creara el objeto como tal que en este caso es nuestro personaje se creara según el contructor seteado ya sea el constructor del personaje uno o el personaje dos.

## Herramientas utilizadas para el desarrollo del proyecto :wrench:

### Editor de código fuente
Un editor de código fuente es un editor de texto diseñado específicamente para editar el código fuente de programas diseñados en lenguajes de programación para este caso utilizamos **Visual Studio Code**

![visualstudio](https://github.com/andressalinas98/EjercicioSprites/blob/master/imagenes/logos/01.jpeg)

### Lenguaje de Programación 
Para este proyecto se utilizo el lenguaje de programación **Python** ya que nos permitia la facilidad de tener un conjunto de módulos para la creacción del tablero y el personaje del juego. Para poder programar en Visual Studio con Python es necesario:

1. Instalar un intérprete de Python en el computador, en este caso fue Python 3.8.2
   Para comprobar que se instalo correctamente python en el computador, en este caso como tenia sistema operativo Windows se abre el        simbolo del sistema y se pone el comando **python --version** si la respuesta es python 3.8.2, quiere decir que fue instalado            correctamente.
2. Instalamos la extensión de Python que tiene Visual Studio Code 

![extensión](https://github.com/andressalinas98/EjercicioSprites/blob/master/imagenes/logos/04.jpeg)

### Pygame
Uyilizamos Pygame porque es un conjunto de módulos del lenguaje Python que permiten la creación de videojuegos en dos dimensiones de una manera sencilla, para poder usarlo lo que debemos hacer es: 

1. Abrimos el simbolo del sistema, en este caso usamos un computador con sistema operativo windows 
2. Ponemos el comando **pip install pygame** donde realizara el proceso de instalacion
3. Para su uso simplemente cuando vayamos a desarrollar el codigo en Visual Studio, en las clases que vayamos la libreria debemos importarla **import pygame**

![pygame](https://github.com/andressalinas98/EjercicioSprites/blob/master/imagenes/logos/02.jpeg)

## Datos de la ejecución del Programa :mag_right:

### Cambiar de personaje 
Para el proyecto contamos con dos jugadores y su cambio se realizara en el codigo, en la clase principal, al setear la fabrica al director lo que debemos hacer es poner **ConstructorJugador_uno()** o **ConstructorJugador_dos()** respectivamente según el personaje que se desee.

La linea de codigo exactamente es: **director.setBuilder(ConstructorJugador_dos())**
## Autores

* **Diana Valentina Uscategui Tobo - 20172020063
* **Edwin Andres Salinas Chaparro - 20172020087
