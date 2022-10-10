# group by, having y drop table

Con `group by` lo que haremos sera crear conjuntos

Los comandos en este apartado son:
 * `group by`
 * `having`
 * `drop table`

Veamos un ejemplo de `group by`, este nos entregara la marca apple y la cantidad de productos apple

<pre>
select count(id), marca from product group by marca;
</pre>

El siguiente fragmento de codigo muestra la cantidad de productos creados por cada usuario

<pre>
select count(p.id), u.name from product p left join user u on u.id = p.created_by group by p.created_by;
</pre>

Podemos usar el comando `having` para obtener resultados certeros, como en el ejemplo anterior que nos puede entregar solo a los que cumplieron cierto rquisito

<pre>
select count(p.id), u.name from product p left join user u 
on u.id = p.created_by group by p.created_by
having count(p.id) >= 2;
</pre>

Para eliminar una tabla usaremos el comando `drop table`, veamos el ejemplo:

<pre>
drop table product;
drop table animales;
drop table user;
</pre>
