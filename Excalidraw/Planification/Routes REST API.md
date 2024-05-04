
---
### Rutas de Registro / Inicio de Sesion: 

- **/  (GET)**
- **/login/  (POST)
- **/register/  (POST)
- **/Help/  (PUT or PATCH, DELETE)    --- Para recuperar, actualizar o eliminar cuenta

### Rutas Para los usuarios: 

- **/users/  (GET)**
- **/users/:param (GET)
- **/users/?username="username"(GET)



- **/users/  (POST - REGISTRAR USUARIO) 
- **/users/  (DELETE - BORRAR USUARIO)
- **/users/  (PUT o PATCH- UPDATE USUARIO)

### Rutas de las Herramientas (Con Middlewares)

- **/tools/  (GET)**
- **/tools/:param  (GET)
- **/tools/?name = nombreHerramienta (GET)

- **/tools/  (POST - CREAR HERRAMIENTA )**
- **/tools/  (DELETE - BORRAR HERRAMIENTA)**
- **/tools/  (PUT - EDITAR HERRAMIENTA)**

### Rutas de las estadisticas: 

- **/statistics/ (GET)
- **/statistics/:param (GET)
- **/statistics/?username=nombreUsuario (GET)
- **/statistics/?username=nombreUsuario (GET)**


- **/statistics/?id=  (PUT ESTADISTICA)**
- **/statistics/?id=  (POST ESTADISTICA)**
- **/statistics/?id=  (DELETE ESTADISTICA)**



### Rutas de Error: 
- 404 or X (Devolver 404.html)