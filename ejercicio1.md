#Ejercicio 1

##postgres.conf


* Modifique el archivo postgres.conf de tal forma que postgres parta en el puerto 8082. Para comprobar que el cambio fue efectivo cree una conexión desde pgAdmin y conectese
* Restaure el puerto por omisión de postgres. Cambie la conexión en pgAdmin y compruebe que el cambio es efectivo
* Modifique el archivo postgres.conf y seleccione como listen_addresses una dirección IP que no corresponda a su equipo. Reinicie y chequee el log para verificar el error. A continuación restaure el valor a localhost
* Utilizando el comando ALTER SYSTEM modifique el valor de la variable shared_buffers al doble. Para obtener el valor de la variable puede utilizar el comando SHOW o realizar un select a pg_settings. Antes de reiniciar verifique sus valores en la tabla pg_settings. Reinicie y verifique los cambios. Explore el archivo postgresql.auto.conf para ver el valor de shared_buffers

##pg_hba.conf

* Modifique el archivo pg_hba.conf de tal forma que rechace todas las conexiones. Chequee que efectivamente las conexiones son rechazadas, intentando conectarse desde el pgAdmin. Una vez hecho esto restaure el archivo pg_hba.conf para que acepte conexiones. Compruebe el buen funcionamiento conectandose desde pgAdmin

##Conexiones
* Conectese al servidor desde pgAdmin. Abrar la herramienta sql. Adicionalmente conectese al servidor a través de psql.
* Monitoree las conexiones viendo los registros de la tabla pg_activity
* Termine la conexión asociada a psql utilizando pg_terminate
* Compruebe que psql pierde la conexión y se conecta nuevamente

##Prueba básica de rol 
* Utilizando pgAdmin cree el rol super usuario llamado todopoderoso, con password todopoderoso y otro rol superusuario llamado super con password super, ambos con derecho a login.
* En el archivo pg_hba.conf limite el acceso de tal forma que solo se pueda conectar el usuario todopoderoso.
* Compruebe via pgAdmin, que el usuario todopoderoso se puede conectar, pero no así el usuario super
* Restaure los valores de pg_hba.conf y reinicie