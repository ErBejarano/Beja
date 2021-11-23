# Proyecto del Primer Cuatrimestre Fundamentos de Programación (Curso 21/22)
Autor/a: Jose Antonio Bejarano Vela; uvus: josbejvel1
  
El proyecto tiene como objetivo analizar los datos de un dataset o bases de datos llamada "NBA player of the week". En la cual nos muestran los datos del jugador de la semana de la NBA que es la maxima categoria de competion de baloncesto en Estados Unidos desde el año 1979 hasta el año 2020. En este dataset encontraremos el nombre del jugador de la semana, el equipo al que pertenece, la conferencia, la fecha del dia, la posicion de juego, la altura, el peso, la edad, año del contrato, temporadas jugando en la liga, temporada actual, temporada, equipo anterior, valor real, jugo la temporada anterior.

Este dataset tiene 5416 líneas de datos y en la primera fila se encuentran los nombres de las respectivas columnas.

## Estructura de las carpetas del proyecto
/data: Contiene el dataset o datasets del proyecto
  - Dataset_NBA.csv: Archivo con los datos de los jugadores de la semana de la NBA.

/src: Contiene los diferentes módulos de Python que componen el proyecto.
  - NBA.py: Contiene funciones para obtener datos .
  - NBA_TEST.py: Contiene funciones de test para probar las funciones del módulo NBA.py.

## Estructura del dataset
Para cada jugador se registran 17 datos. Por lo tanto, el dataset está compuesto por 17 columnas, con la siguiente información:

  - **Player**: apellido y nombre del jugador. Es una cadena de caracteres(str).
  - **Team**: equipo en el que juega. Es una cadena de caracteres(str).
  - **Conference**: confederacion en la que juega. Es una cadena de caracteres(str).
  - **Date**: fecha en la que fue jugador de la semana. Es un dato tipo date.
  - **Position**: posicion en la que juega. Es una cadena de caracteres(str).
  - **Height**: altura en pulgadas. Es un dato tipo float.
  - **Weight**: peso en pulgadas. Es un dato tipo entero(int).
  - **Age**: edad del juagador. Es un dato tipo entero(int).
  - **Darft_Year**: año en el que se unió al equipo. Dato tipo entero(int).
  - **Seasons_in_league**: temporadas jugando en la liga. Dato tipo entero(int).
  - **Season**: temporada en la que consiguió ser el jugador de la semana. Dato tipo entero(int).
  - **Season_short**: temporada en la que consiguió ser el jugador de la semana pero solo en el año que lo fue. Dato tipo entero(int).
  - **Pre_draft_Team**: equipo anterior en el que jugó. Es una cadena de caracteres(str).
  - **Real_value**: valor real del jugador. Es un dato tipo float.
  - **Height_CM**: altura en centímetros. Dato tipo entero(int).
  - **Weight_KG**: peso en kilogramos. Dato tipo entero(int).
  - **Last_Season**: indica si jugó la temporada pasada. Dato tipo boolean.

## Tipos implementados
Para trabajar con los datos del dataset se ha definido la siguiente tupla con nombre:
                                              
`Registro=namedtuple('Registro','Player,Team,Conference,Date,Position,Height,Weight,Age,Draft_Year,Seasons_in_league,Season,Season_short,Pre_draft_Team,Real_value,Height_CM,Weight_KG,Last_Season')`

He transformado los datos la última columna. Eran datos de tipo cadena de caracteres ahora son tipo bool. El cambio es el siguiente:
  - Para el dato "Last_Season" del dataset lo hemos convertido a tipo boolean.

## Funciones implementadas
En este proyecto se han implementado las siguientes funciones en diferentes módulos. Las funciones están clasificadas según los bloques y tipos de funciones que se requieren en cada una de las entregas. El módulo principal es el módulo NBA.py. Es en este módulo donde se hará referencia a cada uno de los bloques de las entregas del proyecto.

## Modulo NBA
## Entrega 1
  * **Bloque 0**
  * **def lee_datos(fichero):** lee los datos del fichero csv y devuelve una lista de tuplas con todos los datos del fichero. Para implementar esta función se han creado las siguientes funciones auxiliares:
    * parse_bool(cadena): Función para convertir de cadena a booleano.
    * parse_date(cadena, formato = "%d/%m/Y"): Función para convertir de cadena a fecha.

## Entrega 2
  ### Bloque 1
  * **def calcula_equipos(datos):** dada una lista de tuplas a traves de la tupla "Registro" que es una nametupled que ese pasa como parmetro de la función. Se toma los datos de los jugadores de la NBA y devuelve una tupla con los nombres de los equipos sin repetir.
  * **def calcular_media_edades(datos):** dada una lista de tuplas de tipo "Registro", devuelve la media de edad de los jugadores cuya información se recoge en la lista de tuplas dada como parámetro.
    * **def filtrar_por_edad(datos):** dada una lista de tuplas de tipo "Registro", devuelve una lista con todas las edades de los jugadores cuya información se recoge en la lista de tuplas dada como parámetro. 

  ### Bloque 2
  * **def jugador_con_mas_altura(datos):** dada una lista de tuplas de tipo "Registro", devuelve una tupla con el nombre de jugador, el equipo al que pertence y su altura, en el momento que PLayer of the Week. La información se recoge en la lista de tuplas dada como parámetro.
  * **def top_jugadores_de_una_confederacion_por_año(datos, temporada, limite=10, confederacion=None):** dada una lista de tuplas de tipo "Registro", devuelve una tupla con el nombre de jugador, las temporadas que lleva en la liga y la fecha en la que consiguio ser PLayer of the Week. Estas tuplas estran filtradas segun los parámetros de la función, puede ser según el año de la temporada y la confederacion. La información se recoge en la lista de tuplas dada como parámetro.
    * **def filtrar_por_temporada** dada una lista de tuplas de tipo "Registro", devuelve una lista con toda la informacion de la tupla "Registro". La información se recoge en la lista de tuplas dada como parámetro y esta estara filtrada por un segundo parametro llamado temporada que es el año en el que se realiza la temporada de la NBA.
  * **def agrupar_por_posicion(datos):** Dada una lista de tuplas de tipo "Registro", devuelve un diccionario en el que las claves representan las posiciones de los jugadores y los valores son listas de los registros que tienen esa posición.

## Modulo NBA_TEST
En este modulo se han definido funciones para probar las funciones del modulo NBA.py. Cada funcion de este módulo se usa para probar la función con que tiene el mismo nombre (pero sin comenzar por test\_ del módulo NBA. Por ejemplo, la función test_lee_datos prueba la función lee_datos.

  - **test_lee_datos()**
  - **test_calcula_equipos()**
  - **test_calcular_media_edades()**
  - **test_jugador_con_mas_altura()**
  - **test_top_jugadores_de_una_confederacion_por_año()**
  - **test_agrupar_por_posicion()**
