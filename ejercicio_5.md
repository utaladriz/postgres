#Ejercicio 5

##Creación de Tablas

Cree un tabla llamada Nodo con las siguientes características:

* campo id serial, asociado a llave primaria pk_nodo
* campo nombre text asociado a restricción de unicidad uq_nodo_nombre
* campo data de tipo jsonb
* campo fecha_creacion de tipo timestamp valor por default la fecha de inserción


Inserte al menos 5 registros.  

Chequee además que existe el tipo asociado a la tabla nodo  

##Creación de Tablas temporales

Cree una tabla temporal llamad temp_nodo utilizando el tipo compuesto asociado a la tabla nodo  
Inserte en la tabla temporal los 5 registros de la tabla nodo.  

Abra una nueva sesión, sin cerrar la actual,  utilizando psql o pgAdmin y compruebe si existe la tabla temporal. Una vez hecho esto cierre las dos sesiones. Vuelva a entrar y comprueba la existencia de la tabla temporal.

##Creación de Tablas Hijas

Ahora cree un tabla denominada Documento que herede de la tabla nodo y que agregue los siguientes campos:

* campo ruta sde tipo text

Inserte registros en la tabla documento al menos 5  
Chequee los registros existentes en la tabla Nodo y en la tabla Documento  
¿Qué sucede? ¿Cuáles son los valores de los ids?  

Inserte ahora un registro en la tabla Documento con el nombre duplicado de un Documento   existente ¿Qué sucede? Verifique los registros de la tabla Nodo y de la tabla Documento  
Inserte ahora un registro en la tabla Nodo con el nombre duplicado de un Nodo existente ¿Qué sucede?  

Ahora examine la tabla Documento y compruebe que restricciones (Constraints posee)   

##Creación de Foreign Key

Ahora cree la tabla llamada Arista con las siguientes caracteríticas:

* campo id serial, asociado a llave primaria pk_nodo
* campo origen foreign key de la tabla Nodo
* campo destino foreign key de la tabla Nodo
* campo data de tipo jsonb
* campo fecha_creacion de tipo timestamp valor por default la fecha de inserción
* Una restricción de unicidad llamada uq_arista_origen_destino de origen y destino

Inserte en la tabla Arista, aristas que conecten los nodos 1->2, 4->2 y 3->5  
Chequee los resultados  
Ahora cree una Arista entre Documentos, por ejemplo 6->8 ¿Es posible?  
Intente borrar el Nodo 1 ¿Es posible?  
Intente ahora agregar una nueva arista entre los nodos 1->2 ¿Es posible?  

##Creación de Tabla sin log
Cree una tabla sin log denominada tabla_sinlog con la siguiente estructura:  

* campo id serial, asociado a llave primaria pk_tabla_sinlog
* campo nombre text

Inserte 5 registros  
Chequee que los registros esten insertados y anote el valor de la secuencia
Mate el proceso asociado a Postgres  
Inicie nuevamente Postgres y chequee la existencia de los registros ¿Existen?
¿Cuál es el valor de la secuencia?













