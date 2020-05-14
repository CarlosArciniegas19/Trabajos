# Registro de COOMICS
Hemos realizado una aplicacion de MVC (modelo-vista-controlador) con el fin de usarse como una biblioteca de "coomics" para un usuario en donde podra registrar sus revistas favoritas o llegado el caso, series favoritas y poder categorizarlas por medio de una "calificacion" que el mismo usuario tendra el atrevimiento de dar al "coomic" por registrar, ademas, la interfaz otorga al usuario un ChartArea que se usara para dar informacion al usuario de todos las historietas registradas y asi mismo, una lista actualizable de sus registros dados y por ultimo, herramientas extras que se hablaran a continuacion. 

![Form1](https://github.com/CarlosArciniegas19/Trabajos/blob/master/97064106_573678496617536_2027945319353810944_n.png "Inicio")

y un boton que permite ir a una nueva venta en la cual puede cambiear los datos del
coomic del cual se presione el boton.Tambien al registrar un coomic se creara un grafica con el nombre del coomic y se medira segun como 
este calificado el coomic.
 
![Form2](https://github.com/CarlosArciniegas19/Trabajos/blob/master/97064104_538006403558205_3994809056932921344_n.png "Actualizacion")


## Lenguaje

Decidimos usar Lenguaje de programacion c# (C sharp) en el Software para programar "Visual Studio" ya que, nos ofrece una aplicacion ".NET" con la que podemos trabajar una interfaz de usuario de manera facil de entender y rapida, su nombre es "Aplicacion de Windows Forms (.NET Framework).

![visual studio](https://github.com/CarlosArciniegas19/Trabajos/blob/master/lightbulb-dark-Still-1200.jpg "Visual")

### Herramientas usadas en Visual Studio 2019

Visual Studio nos ofrece la posibilidad de manejar sus herramientas de una forma de "arrastrar-pegar" donde literalmente seleccionabamos en la lista de herramientas la que necesitabamos y la pegabamos en la interfaz en blanco. De esta forma, si seleccionabamos una herramienta ya insertada, podiamos acceder tanto a sus eventos como a sus propiedades y modificarlas.
Para el software fueron usados las siguientes herramientas:
* TextBox(Controles Comunes).
* Button(Controles Comunes).
* Label (Controles Comunes).
* Check Box (Controles Comunes).
* FlowLayoutPanel(Contenedores).
* Panel(Contenedores).

####TextBox utilizados en la aplicacion:


Estas cajas de texto, seran utilizadas para el registro que haga el usuario en la interfaz por lo tanto, las mas importantes en este proyecto respecto al requisito del usuario son la que registra el nombre del "COOMIC" y la "Calificacion" por parte del usuario ya que, son los registros que se evaluaran en la lista de registros (el cual esta dentro de un "FlowLayoutPanel") y en el graficador de columnas (el cual se encuentra dentro de una herramienta "Panel").
Cabo destacar que, todas estas cajas de texto han sido programadas ya que,  se usaran los datos para ser transportados por medio de POO de un lado a otro, entre clases, controles de usuario y librerias.

####Button utilizados en la aplicacion:


Los Button son la herramienta mas programada en nuestro proyecto ya que, por medio del evento "click" por parte del usuario, sera el factor clave para activar toda clase de casos de procesamiento necesario para dar funcionalidad al proyecto. Algunos de los Button mas importantes son los siguientes:

* En este boton encontramos en su codigo fuente un proceso de comparacion, donde validamos por medio de una funcion llamada "ValoresVacios()" si algun campo de las cajas de texto se encuentran vacias y llegado el caso, informarle al usuario que hacen falta campos por completar. En caso contrario, el usuario habra hecho todos los registros y asi se llevara ha cabo, la creacion de un graficador de columnas y la biblioteca de "COOMICS".

* En este boton encontramos en su codigo fuente un proceso de actualizacion de registros donde el contenido de las cajas de texto del segundo formulario sera el nuevo dato de los registros ingresados por el usuario anteriormente, y por ultimo, proceder a cerrar el formulario.

####Labels utilizados en la aplicacion:

Los Labels en nuestro proyecto, tomaran el rol de ser los enunciados que informaran al usuario de que tratara cada campo por registrar o seleccionar y por ende, sus propiedades deben ser lo mas atractivas o legibles posibles para el usuario.

####FlowLayoutPanel utilizados en la aplicacion:

Implementamos este tipo de panel, con la intencion de ahorrarnos codigo y tiempo a la necesidad de crear la biblioteca de registros del usuario, ya que, esta herramienta nos proporciona la creacion de nuestros registros u objetos de una forma ordenada y asi no hacer tan complejo el asunto.

####Panel utilizados en la aplicacion:

Implementamos esta herramienta para el graficador de columna, por que era el mas ocasional para el requisito ya que, realmente solo necesitamos crear un "objeto" o por asi decirlo un graficador y por eso, no tuvimos ni siquiera la necesidad de tocar la propiedad de "AutoScroll" por que modificamos su tamaño para que sea equivalente al del graficador.


##CONTENIDO DE NUESTRO "PROYECTO SOLUCION"

#### "cs_Coomics.cs"

Es una clase en la que encontraremos las variables del registro por parte del usuario, estas deben ser privadas para que nadie obtenga acceso a ellas directamente asi que, para poder ser procesadas en los formularios o en otras clases, hemos hecho el encapsulamiento de estas para que puedan ser modificadas o retornadas.

#### "cs_Validacion.cs"

Es una clase en la que encontraremos dos funciones publicas, las cuales tendran como parametro el evento de presionar una tecla, de esta forma, al recibir el parametro podremos verificar por medio de una comparacion de metodos para caracteres, si la tecla presionada es caracter tipo letra, separador, etc. De esta forma, podremos informar al usuario que debe registrar exactamente en cada campo del formulario.

#### "f_Ayuda.cs"

Sera la clase que tomaremos como referencia o como herencia para implementar el button "AYUDA" en nuestros formularios de registros del usuario, con el fin ofrecer un formulario al usuario para contacto o soporte.

#### "Form1.cs"

Es nuestra clase principal ya que, es la que contiene la interfaz principal de nuestro proyecto

#### "Form2.cs"

Es nuestra clase en donde tendremos de entrada algun tipo de registro del usuario de la biblioteca de "COOMICS" y en donde podremos llegado el caso, retornar un nuevo registro y de esa forma realizar una actualizacion (mencionando la herramienta "CheckBox").

#### "Form3.cs"

Esta sera la clase que usaremos como formulario de contacto o soporte para el usuario, el cual se abrira por medio del button "AYUDA" que hereda la clase "Form1" de la clase "f_Ayuda.cs".

#### "Res.en-US.resx"

Este sera nuestro archivo de recursos en el cual usaremos como referencia para el cambio de idioma o cambio del valor de la propiedad "Text" de las Herramientas utilizadas al idioma Ingles.

#### "Res.resx"

Como en el caso anterior, sera un archivo de recursos el cual es nuestro principal por ser el idioma "Cultural" de nuestro ordenador y por ende, hara el cambio de idioma a Español-españa(ES).

#### "UC_Coomics.cs"

Sera nuestra clase o elemento tipo "Control de usuario" que se encargara de la interfaz de cada registro que se incorpora dentro del "FlowLayoutPanel" y de esta forma, hara la creacion de una biblioteca de "COOMICS". Ademas, este "control de usuario" no solo contiene los registros retornados sino, tambien un button con el cual hara la creacion del segundo formulario para dar paso a una actualizacion del registro.

![herramientas](https://github.com/CarlosArciniegas19/Trabajos/blob/master/uRHYM.png "Cosas")

##DLL

*dll_suma

Esta libreria fue creada con la intencion de realizar un metodo o funcion que pueda sumar los numeros de un dato recibido como parametro string, el cual sera enviado tambien como parametro string a una funcion de la  segunda clase dentro de la libreria donde el string se convertira en entero para ser tratado en un algoritmo y de esa forma poder retornar la suma a la primera clase y luego esta clase retornara el entero a donde sea utilizada.

![DLL](https://github.com/CarlosArciniegas19/Trabajos/blob/master/97016953_746579532545529_7158644724952203264_n.png "Nombre")
![DLL](https://github.com/CarlosArciniegas19/Trabajos/blob/master/97125092_910095506115891_7702595508287569920_n.png "Codigo")


*dll_chart

El funcionamiento de esta libreria consiste en un "control de usuario" el cual contiene un metodo llamado "DatosIngresados" el cual recibira como parametro un dato entero (Califacion del "COOMIC") y un dato cadena (Nombre del "COOMIC"), los cuales se usaran como argumento para realizar la creacion de de los puntos de una "Serie" de un graficador tipo "Chart" con todas sus propiedades y al mismo tiempo, realizar la comparacion de dos colores en los cuales en cierta posicion de los puntos de la serie seran aplicados en la graficacion de la columna, ademas, la interfaz de este "control de usuario" contiene tambien un button el cual en su evento "click" se encargara de mostrar o no mostrar el valor de la calificacion del "COOMIC" registrada por el usuario como un Label en la parte superior de la Columna graficada.


![DLL](https://github.com/CarlosArciniegas19/Trabajos/blob/master/97405174_2553990268175243_8062636401893572608_n.png "Nombre")

![DLL](https://github.com/CarlosArciniegas19/Trabajos/blob/master/98342966_2732546470336600_5263212293574885376_n.png "Codigo")
