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

