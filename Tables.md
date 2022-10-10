# Insert, alter table y show create table

Los comandos en este apartado son:
 * `INSERT INTO <nombre_tabla>(tipo, estado) VALUES("valor_tipo", "valor_estado");`
 * `ALTER TABLE <nombre_tabla> MODIFY COLUMN <nombre<_columna> int auto_increment;`
 * `SHOW CREATE TABLE <nombre_tabla>;`
 * `--` (para escribir comentarios)

Para insertar datos usaremos el comando `INSERT INTO animales(tipo, estado) VALUES("chanchito", "feliz");`, sin embargo, primero deberemos hacer que autoincremente su valor, para eso seguimos el siguiente procedimiento:
  `ALTER TABLE animales MODIFY COLUMN id int auto_increment;` lo seleccionamos y damos al icono del rayo, ahora si podremos modificar la tabla y dar clic al icono del rayo. Si queremos ver nuestra tabla usaremos el comando `SHOW CREATE TABLE animales;` y se mostrara el comando para crear la tabla, copiamos y pegamos lo que aparece

<pre>
create database Hola_Mundo;
show databases;
use Hola_Mundo;
CREATE TABLE animales(
	id int,
    tipo varchar(255),
    estado varchar(255),
    PRIMARY KEY (id)
);
INSERT INTO animales(tipo, estado) VALUES("chanchito", "feliz");

ALTER TABLE animales MODIFY COLUMN id int auto_increment;

SHOW CREATE TABLE animales;

CREATE TABLE `animales` ( # Comando que copiamos
   `id` int NOT NULL AUTO_INCREMENT,
   `tipo` varchar(255) DEFAULT NULL,
   `estado` varchar(255) DEFAULT NULL,
   PRIMARY KEY (`id`)
 )  
</pre>

Ahora la linea de `INSERT INTO animales(tipo, estado) VALUES("chanchito", "feliz");` le agregamos dos lineas al principio, la copiamos y pegamos al final, aprovechamos para insertar otros datos y lo ejecutamos

<pre>
INSERT INTO animales(tipo, estado) VALUES("chanchito", "feliz");
INSERT INTO animales(tipo, estado) VALUES("vaquita", "feliz");
INSERT INTO animales(tipo, estado) VALUES("conejito", "feliz");
</pre>
