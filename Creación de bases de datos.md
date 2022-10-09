# Introducción

Una base de datos se encarga de contener varias tablas, pero antes debemos crear nuestra base de datos.

# Tipos de datos

Los tipos de datos son los siguientes:
  * `int`: Numeros enteros (0,1,2,3,...)
  * `float`: Numeros con decimales (12.654,...)
  * `varchar`: Cadenas de texto ("Hola Mundo"), se debe ingresar que tan larga será la cadena

Los comandos en este apartado son:
 * `create database <nombre>;`
 * `show databases;`
 * `CREATE TABLE animales();`
 * `PRIMARY KEY (nombre_columna)`
 * `use <nombre_base_datos>`

# Creando nuestra base de datos

Comenzamos ingresando el comando `create database Hola_Mundo;` y lo ejecutamos, para eso daremos clic al icono de rayo, a conctinuación veremos que se ha creado nuestra base abajo de nuestra linea de comandos

<pre>
[in] create database Hola_Mundo;
[out] create database Hola_Mundo	1 row(s) affected	0.125 sec
</pre>

Si queremos ver todo el registro de bases de datos que se encuantra gestionando SQL usamos el comando `show databases;`, cabe resaltar que si queremos que se ejecute deberemos seleccionar el comando y darle otra vez al icono del rayo

<pre>
[in] show databases;
[out] # Nos muestra las bases de datos creadas
</pre>

Ahora que hemos creado nuestra base de datros, crearemos una tabla con el comando `CREATE TABLE animales();`, no termina ahi, deberemos ingresar las columnas dentro del parentesis junto a un identificador y su tipo de dato.
Indicamos el tipo de dato que será nuestro identificador (int), el tipo (varchar) junto a su longitud, estado (varchar), el `PRIMARY KEY (id)` para que sirva como identificador e indicarle  la base de datos que vamos a usar para esta tabla `use Hola_Mundo`.
Ahora seleccionamos el `use Hola_Mundo` y damos clic al icono del rayo, despues de eso ya podemos seleccionar `CREAT TABLE` y darle al icono del rayo.

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
</pre>












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

# select, update y delete

Los comandos en este apartado son:
 * `INSERT INTO <nombre_tabla>(tipo, estado) VALUES("valor_tipo", "valor_estado");`
 * `SELECT * FROM <tabla>`
 * `SELECT * FROM <tabla> WHERE id = n`
 * `SELECT * FROM <tabla> WHERE estado = 'palabra'`
 * `AND`
 * `UPDATE`
 * `DELETE`
 * `f`

Si queremos listar todos los registros que hemos ingresado usaremos el comando `SELECT * FROM animales` y se mostrara la tabla

<pre>
SELECT * FROM animales;
</pre>

Si queremos buscar un solo registro usaremos el comando `SELECT * FROM animales WHERE id = 1` y se mostrara la primera fila

<pre>
SELECT * FROM animales WHERE id = 1
</pre>

Tenemos otra forma de buscar con el comando `SELECT * FROM animales WHERE estado = 'feliz'`, este nos puede devolver mas de un registro

<pre>
SELECT * FROM animales WHERE estado = 'feliz'
</pre>

Otra manera es agregar el operador `AND`
<pre>
SELECT * FROM animales WHERE estado = 'feliz'AND tipo = 'chanchito';
</pre>

Para actualizar los registros dentro de nuestra base de datos usaremos el comando `UPDATE` y con `SELECT * FROM animales;` veremos que se ha actualizado la tabla

<pre>
UPDATE animales SET estado = 'triste' WHERE id = 3;
SELECT * FROM animales;
</pre>

Si queremos borrar usamos el comando `DELETE` **Y RECUERDA, CUIDADO CON EL WHERE, ¿CREES QUE LOS MEMES DE QUE BORRARON LA BASE DE DATOS CON UN WHERE ES BROMA? TEN CUIDADO CON EL WHERE O VALDRAS VRG**

<pre>
DELETE FROM animales WHERE estado = 'feliz'; -- Esto te borraria la base de datos, cuidado
DELETE FROM animales WHERE id = 1; -- Esto si está bien
</pre>

Si intentamos actualizar obtendremos un error, para evitar esto deberemos agregar el id 

<pre>
UPDATE animales SET estado = 'triste' WHERE tipo = 'conejito'; -- Esto te dará un error
</pre>

# Condiciones en profundidad

<pre>

</pre>

<pre>

</pre>

<pre>

</pre>

<pre>

</pre>
<pre>

</pre>

<pre>

</pre>

<pre>

</pre>

<pre>

</pre>
<pre>

</pre>

<pre>

</pre>

<pre>

</pre>

<pre>

</pre>
