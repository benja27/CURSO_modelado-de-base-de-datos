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