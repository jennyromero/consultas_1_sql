# consultas_1_sql
 # Introducción a las consultas a una BD usando el lenguaje SQL

## Base de datos: Ventas
## Tabla: Cliente

![Tabla Cliente](tabla_cliente.png)

## Instrucciones SELECT
- Permite seleccionar datos de una tabla.
- Su formato es: `SELECT campos_tablas FROM
nombre_tabla``

### Consultas No. 1
1. Para visualizar toda la informacion que contiene la tabla Cliente se puede incluir con la instruccion SELECT el caracter **\*** o cada uno de los campos de la tabla.

- `SELECT * FROM Cliente`
- `SELECT identificacion, nombre, apellidos, direccion, telefono,ciudad_nac, fecha_nac FROM Cliente`
