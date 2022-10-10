# select, update y delete

Los comandos en este apartado son:
 * `INSERT INTO <nombre_tabla>(tipo, estado) VALUES("valor_tipo", "valor_estado");`
 * `SELECT * FROM <tabla>`
 * `SELECT * FROM <tabla> WHERE id = n`
 * `SELECT * FROM <tabla> WHERE estado = 'palabra'`
 * `AND`
 * `UPDATE`
 * `DELETE`

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

