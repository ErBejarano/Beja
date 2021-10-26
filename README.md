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
### Modulo NBA
#### Entrega 1
  * **Bloque 0**
  * **def lee_datos(fichero):** lee los datos del fichero csv y devuelve una lista de tuplas con todos los datos del fichero. Para implementar esta función se han creado las siguientes funciones auxiliares:
    * parse_bool(cadena): Función para convertir de cadena a booleano.
    * parse_date(cadena, formato = "%d/%m/Y"): Función para convertir de cadena a fecha.

### Modulo NBA_TEST
En este modulo se han definido funciones para probar las funciones del modulo NBA.py. Cada funcion de este módulo se usa para probar la función con que tiene el mismo nombre (pero sin comenzar por test\_ del módulo NBA. Por ejemplo, la función test_lee_datos prueba la función lee_datos.

  - **test_lee_datos()**
