#Ejercicio 2

##Configuración
Asegurese que la configuracion de Postgres sea DMY e ISO

##Crear una base de datos
Cree una base de datos llamada figuras  
En esa base de datos cree tablas para almacenar figuras geométricas:  

* Circulo (x,y del centro y radio)  
* Cuadrado (x,y esquina superior izquierda y lado)  
* Cruz (x,y centro y radio)
 
Todos los elementos deben incluir un atributo llamado fecha de creación que contiene el timestamp con dicha fecha.  
Todos los elementos deben un identificador único (Id).

Inserte al menos tres registros por tabla.

##Backup
Realice un full dump de la base de datos  
Relice un backup de la base de datos en SQL TEXT PLAIN  
Modifique el backup SQL TEXT PLAIN agregando algunos insert de figuras

##Restauración Parcial
Haga un drop de la base de datos   
Restaure solo la estrucutura de la base de datos  
Comprueba que la estructura está creada 
Luego importe los datos utilizando psql con el arcchivo backup SQL TEXT PLAIN

##Restauración completa
Haga un drop de la base de datos   
Restaure de manera completa la base de datos a partir del backup

##Tipo Compuesto
Cree un tipo compuesto para las figuras que contenga los campos x,y y radio   
Cree un esquema denominado "nuevo"
En ese esquema cree las  figuras geométricas:  

* Circulo 
* Cuadrado 
* Cruz 

Pero utilizando el nuevo tipo compuesto Figura.






