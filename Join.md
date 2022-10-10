# left join

Los comandos en este apartado son:
 * `foreign key (<nombre_tabla)`
 * `references user(<nombre_columna>)`
 * `rename`
 * `left join`

Abrimos una nueva pestaña, crearemos una nueva tabla para cruzar con la tabla de usuarios para colocar llaves foraneas. `foreign key (created by)` con este comando estamos indicando que es una llave foranea, ahora usaremos un nuevo comando para decirle de que tabla esta haciendo referencia con el comando `references user(id)`

<pre>
create table products(
	id int NOT NULL AUTO_INCREMENT,
    name varchar(50) not null,
    created_by int not null,
    marca varchar(50) not null,
    PRIMARY KEY (id), 
    foreign key (created_by) references user(id)
 );
</pre>

Pra renombrar las tablas usamos el comando `rename`

<pre>
rename table products to product; 
</pre>

Para insertar multiples datos en una sola columna haremos lo siguiente, al final seleccionamos todo y lo ejecutamos

<pre>
 insert into product (name, created_by, marca)
 values
	('ipad',1,'apple'),
    ('iphone',1,'apple'),
    ('watch',2,'apple'),
    ('macbook',1,'apple'),
    ('imac',3,'apple'),
    ('ipad mini',2,'apple');
</pre>

Ahora haremos un left join, esto nos arrastrara todos los datos en la tabla de usuarios y si es que hay datos en la tabla de productos los traera.

<pre>
select u.id, u.email from user u;
-- el left join se hara a continuacion
select u.id, u.email, p.name from user u left join product p on u.id = p.created_by;
</pre>

# Right join

Los comandos en este apartado son:
 * `right join`
 * `inner join`

El right join es lo mismo, pero por la derecha. Veamos un ejemplo:

<pre>
select u.id, u.email, p.name from user u right join product p on u.id = p.created_by;
</pre>

Para el inner join solo tomaremos la interseccion entre ambas tablas, veamos un ejemplo:

<pre>
select u.id, u.email, p.name from user u inner join product p on u.id = p.created_by;
</pre>

# cross join

El cross join te entrega el producto cartesiano entre ambas tablas, es decir, una regla de la multiplicacion con tablas. Cabe mencionar que la cantidad de informacion puede ser potencialmente grande

Los comandos en este apartado son:
 * `cross join`

<pre>
select u.id, u.name, p.id, p.name from user u cross join product p;
</pre>
