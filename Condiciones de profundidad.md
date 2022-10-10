# Condiciones en profundidad

Los comandos en este apartado son:
 * `LIMIT`
 * `OR`
 * `BETWEEN`

Para este apartado crearemos una nueva tabla con sus respectivos datos

<pre>
CREATE TABLE user (
   id int NOT NULL AUTO_INCREMENT,
   name varchar(50) not null,
   edad int not null,
   email varchar(100) not null,
   PRIMARY KEY (id)
 );
 
INSERT INTO user(name, edad, email) VALUES('Oscar',25,'oscar@gmail.com');
INSERT INTO user(name, edad, email) VALUES('Layla',15,'layla@gmail.com');
INSERT INTO user(name, edad, email) VALUES('Nicolas',36,'nico@gmail.com');
INSERT INTO user(name, edad, email) VALUES('Richie',23,'richie@gmail.com');
</pre>

El comando `LIMIT` nos devolvera unicamente la cantidad de recursos que le encomendemos

<pre>
select * from user limit 1;
</pre>

Tambien podemos buscar con limites de datos, ejemplo:

<pre>
select * from user where edad >15;
select * from user where edad >=15;
select * from user where edad >20 and email = 'oscar@gmail.com';
select * from user where edad >20 or email = 'layla@gmail.com';
select * from user where email != 'layla@gmail.com';
select * from user where edad between 15 and 30;
select * from user where email like '%gmail%';
select * from user where email like '%gmail'; -- la busqueda debe terminar en gmail
select * from user where email like 'gmail%'; -- la busqueda debe empezar en gmail
select * from user order by edad asc; -- los ordena en orden ascendente por su edad
select * from user order by edad desc; -- los ordena en orden descendente por su edad
select max(edad) as mayor from user; -- nos devuelve la mayor edad, solo el numero 
select min(edad) as menor from user; -- nos devuelve la menor edad, solo el numero 
</pre>
