# EN ESTE CURSO APRENDEREMOS MODELADO DE BASES DE DATOS

## se va a generar una base de datos de una tienda en linea

## lista de entidades (tablas)

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono 
- email 
- direccion
- codigo postal
- ciudad 
- pais **(FK)**

### productos **(ED) | (EC)**

- producto_id **(PK)**
- nombre
- descripcion
- foto 
- precio
- cantidad 

### ventas **(ED)**

- venta_id **(PK)**
- cliente  **(FK)**
- fecha 
- monto 


## articulos_x_venta **(EP)**
- articulo_id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad **()**


### pais **(EC)**
- pais_id
- nombre 
- dominio

## RELACIONES

1. Un **cliente** tiene **pais** (1 - 1)
2. Una **cliente** hace **ventas** (1 - M)
2. Una **venta** tiene **articulos** (1 - M)
2. Una **articulo** es un **producto** (1 - M)


## reglas de negocio 

## clientes
* crear un cliente
* leer todos los clientes
* actualizar un cliente
* eliminar un cliente 

## productos
* crear un producto
* leer todos los productos 
* leer un producto en particular
* actualizar un producto 
* eliminar un producto
* cada que haya una venta restar la cantidad de productos disponibles al stock


## ventas 

* crear una venta
* leer todas las ventas
* leer una venta en particular
* leer todas las ventas de un cliente 
* leer todas las ventas de un producto
* actualizar una venta 
* eliminar una venta 

## articulos por venta 
* crear un articulo 
* leer todos los articulos
* leer un articulo en particular
* leer todos los articulos de una venta 
* leer todos los articulos de un producto 
* leer todos los articulos de un cliente 
* actualizar un articulo
* eliminar un articulo

## paises 
* crear un pais 
* leer todos los paises 
* leer un pais en particular 
* actualizar un pais 
* eliminar un pais 


# MODELADO PARA UN SISTEMA DE AUTENTIFICACION

## * Lista de entidades  ---->


## usuarios **(ED)**

- usuario_id **(PK)**
- user_name  **(UQ)**
- password 
- email **(UQ)**
- nombre
- apellido
- avatar
- activo 
- fecha_creacion
- fecha_actualizacion

## roles **(EC)**

- rol_id **(PK)**
- nombre 
- descripcion


## permisos **(EC)**

- permiso_id **(PK)**
- nombre 
- description 

## roles_x_usuarios **(EP)**

- rxu_id **(PK)**
- usuario_id **(FK)**
- rol_id **(FK)**

## permisos_x_roles **(EP)**

- pxr_id **(PK)**
- rol_id **(FK)**
- permiso_id **(FK)**


## Relaciones de este sistema ---->

1. **usuarios** tienen **roles** (M - M)
2. **Roles** tienen **permisos** (M - M)

## despues de esto se genera el diagrama en diagrams.net ------>


## GENERAR LAS REGLAS DEL NEGOCIO 

### usuarios

1. crear un usuario 
2. leer todos los usuarios 
3. leer un usuario 
4. actualizar un usuario 
5. validar un usuario
6. habiliatar un usuario 
7. inabilitar un usuario 
8. actualizar datos de un usuario 
9. actualizar password de un usuario 
10. eliminar un usuario 

### roles 

1. crear un rol
2. leer todos los roles 
3. leer un rol en particular
4. actualizar un rol 
5. eliminar un rol 


### permisos 

1. crear un permiso
2. leer todos los permisos 
3. leer un permiso en particular 
4. actualizar un permiso 
5. eliminar un permiso 

### roles_x_usuario

1. crear un rxu
2. leer todos los rxu 
3. leer un rxu en particular 
4. leer todos los rxu de un usuario 
5. eliminar un rxu 


### permisos por roles 

1. crear un pxr
2. leer todos los pxr 
3. leer un pxr en particular 
4. leer todos los pxr de un rol 
5. eliminar un pxr 
