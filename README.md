# consultas_1_sql

# Introducción a las consultas a una BD usando el lenguaje SQL

## Base de datos: Ventas

## Tabla: Cliente

![Tabla Cliente](tabla_cliente.png)

## Instrucciones SELECT

- Permite seleccionar datos de una tabla.
- Su formato es: `SELECT campos_tablas FROM nombre_tabla`

### Consultas No. 1

1. Para visualizar toda la informacion que contiene la tabla Cliente se puede incluir con la instruccion SELECT el caracter **\*** o cada uno de los campos de la tabla.

- `SELECT * FROM Cliente`
  ![Consulta 1](consultas_1.png)

- `SELECT identificacion, nombre, apellidos, direccion, telefono,ciudad_nac, fecha_nac FROM Cliente`
  ![Consulta 1](consultas1_2.png)

### Consultas No. 2

2. Para visualizar solamente la identificacion del cliente : `SELECT identificacion FROM Cliente`
   ![Consulta 2](consultas2.png)

### Consultas No. 3

3. Si se desea obtener los registros cuya identificacion sea mayor o igual a 150 se debe utilizar la clausula `WHERE` que especifica las condiciones que deben reunir los registros que se van a seleccionar: `SELECT * FROM Cliente WHERE identificacion>=150`
   ![Consulta 3](consultas3.png)

### Consulta No. 4

4. Se desea obtener los registros cuyos apellidos seana Vanegas o Cetina, se debe utilizar el operador `IN` que especifica los registros que se quieren visualizar de una tabla.

`SELECT apellidos, nombre  FROM Clientes WHERE apellidos IN ('Vanegas','Cetina')`

![Consulta 4](consultas4.png)
o se puede utilizar el operador `OR`

`SELECT apellidos,nombre  FROM Clientes WHERE apellidos = 'Vanegas' OR apellidos = 'Cetina'`
![Consulta 4](consulta4_2.png)

### Consulta No. 5

5. Se desea obtener los registros cuya identificacion sea menor de 110 y la ciudad sea cali, se debe utlizar el operador `AND`

`SELECT * FROM Cliente WHERE identificacion<=110 AND ciudad_nac = 'Cali'`

![Consulta 5](consultas5.png)

### Consulta No. 6

6. Si se desea obtener los registros cuyos nombres empiecen por la letras 'A', se debe utilizar el operador `LIKE`que utiliza los patrones `%` (todos) y `_` (caracter).

`SELECT * FROM Cliente WHERE nombre LIKE 'A%'`
![Consulta 6](consultas6.png)

### Consultas No. 7

7. Se desea obtener los registros cuyos nombre contengan la letra 'a'

`SELECT * FROM Cliente WHERE nombre LIKE '%a%'`
![Consulta 7](consultas7.png)

### Consultas No. 8

8. Se desea obener los registros donde la cuarta letra del nombre del cliente sea la letra 'a'

`SELECT * FROM Cliente WHERE nombre LIKE '___a'`
![Consulta 8](consultas8.png)

### Consultas No. 9

9. Si se desea obtener los registros cuya identiicacion este entre el intervalo 110 y 150, se debe utilizar la clausula 'BETWEEN', que sirve para especificar un intervalo de valores.

`SELECT * FROM Cliente WHERE identificacion BETWEEN 110 AND 150`
![Consulta 9](consultas9.png)

## Instrucción DELETE

- Permite borrar todos o un grupo especifico de registros de una tabla.
- Su formato es: ` DELETE FROM nombre_tabla`

### Eliminación No. 1

1. eliminar los registros cuya identificacion sea mayor a 150

`DELETE FROM Cliente WHERE identificacion > 150`

![Eliminacion 1](eliminacion1.png)

2. Eliminar los registros cuya identificacion sea igual a 116

`DELETE FROM Cliente WHERE identificacion = 116`

## Instrucción UPDATE

- Permite actualizar un campo de una tabla.
- Su formato es: `UPDATE nombre_tabla SET nombre campo = valor`

### Actualizacion No. 1

1. Para actualizar la ciudad de nacimiento de Cristian Vanegas, cuya identificacion es 114

`UPDATE Cliente SET ciudad_nac = 'Pereira' WHERE identificacion=114`

![Actualizacion ](actualizacion1.png)

## Creacion tabla Pedido

### Diccionario de datos

| Campo              | Tipo de dato | Longitud |
| ------------------ | -----------  | -------- |
|***no_pedido**      | varchar | 15 |
| iden_cliente       | varchar | 15 |
| fecha_compra       | date    | |
| fecha_vencimiento  | date    |  |
|observacion| varchar|30|


### Modelo Entidad - Relacion 

![Modelo ](modelo.png)

