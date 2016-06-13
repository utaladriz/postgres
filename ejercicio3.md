#Ejercicio 3

##Tipos
Cree un tabla llamada Persona que contenga los siguientes campos :  

* id de tipo serial 
* nombre text
* apellido paterno text
* apellido materno text
* fecha de nacimiento de tipo date
* fecha de creación de tipo timestamp
* tipo de persona que sea un range smallint de 1 a 3
* identificador text
* habilitado boolean

Cree un tabla llamada Direccion que contenga los siguientes campos :  

* id de tipo serial 
* direccion text
* numero paterno text
* piso materno text
* ciudad tipo text
* localidad tipo text
* zip text
* habilitado boolean

Inserte al menos 5 registros por tabla. Trate de ocupar los diferentes formatos de fecha.  
Luego realice consultas ocupando filtros por cada campo.

(Tiempo estimado 20 Minutos)

##Arreglos
Cree un tabla llamada ventas que contenga los siguientes campos :  

* id de tipo serial 
* ano int range entre 2015 a 2030
* ventas_mensuales arreglo int de 1 a 12

Cree un tabla llamada proyeccion que contenga los siguientes campos :  

* id de tipo serial 
* ano int range entre 2015 a 2030
* ventas_mensuales arreglo int de 1 a 12



Inserte al menos 5 registros por tabla. 
Luego realice una consulta que muestre la diferencia entre las ventas y lo proyectado para cada mes dado un año. 

(Tiempo estimado 15 Minutos)





