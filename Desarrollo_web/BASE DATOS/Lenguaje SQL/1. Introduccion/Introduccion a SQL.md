
---
# **Bases de Datos SQL (Structured Query Language):**

### ¿Para que sirve SQL ?

Nos permite crear y administrar bases de datos, es decir el proposito CRUD, que se basa en crear, leer, actualizar y borrar datos de una base de datos. Tambien nos permite hacer consultas a la BD, ademas de añadir reglas o condiciones que permitan filtrar los datos para que sean correctos.

### Sub Lenguajes:

- DML (Data Manipulation Languaje):
    
    Simplificado: Realiza el CRUD (Create, Read, Update y Delete)
    
    Se centra en la manipulación de datos en una base de datos. Incluye comandos como **`INSERT INTO`** para realizar acciones como el CRUD.
    
- DDL (Data Definition Languaje):
    
    Simplificado: Crea las tablas.
    
    Trata sobre la definición de la estructura de la base de datos. Con DDL, puedes crear tablas (**`CREATE TABLE`**).
    
- DCL (Data Control Languaje):
    
    Simplificado: Administra los permisos de las personas que acceden a la base de datos.
    
    Está relacionado con la gestión de permisos de acceso a la base de datos. **`GRANT`** permite otorgar permisos a usuarios o roles, y **`REVOKE`** los revoca.
    
- TCL (Transaction Control Languaje):
    
    Simplificado: Realiza transacciones y confirma sus cambios.
    
    Se utiliza para controlar las transacciones en una base de datos. **`COMMIT`** confirma los cambios en una transacción, mientras que **`ROLLBACK`** deshace los cambios no confirmados. **`SAVEPOINT`** establece puntos de guardado dentro de una transacción.
    
- CSL (Session Control Languaje):
    
    Permite configurar opciones de sesión específicas para la sesión de trabajo actual. Esto puede incluir configuraciones como el formato de fecha y hora o el nivel de aislamiento de transacción.
    
- DQL (Data Query Languaje):
    
    Simplificado: Muestra datos de las consultas, clausula SELECT
    
    Trata sobre la recuperación de datos de una base de datos utilizando la sentencia **`SELECT`**. Puedes especificar qué datos deseas obtener, filtrarlos, agruparlos y ordenarlos según tus necesidades.
