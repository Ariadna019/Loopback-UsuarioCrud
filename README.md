# usuarios-crud

LoopBack CRUD con MySQL
Este proyecto es una API REST creada con LoopBack que permite gestionar información a través de un CRUD (Create, Read, Update, Delete). Se conecta con una base de datos MySQL y permite interactuar con la información mediante Postman o directamente con LoopBack Explorer.



Configuración de la Base de Datos:
Este proyecto usa una base de datos llamada usuario-crud, que contiene una tabla usuario.

Si la base de datos aún no existe, puedes crearla manualmente en MySQL:


CREATE DATABASE usuario_crud;
USE usuario_crud;

CREATE TABLE usuario (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    edad INT NOT NULL
);

Para que te funcione el codigo de api rest con loopback con mi base de datos es necesrio que cumplas estos pasos:

Primer paso:debes clonar el repositorio a tu computadora 
```sh
git clone  https://github.com/Ariadna019/Loopback-UsuarioCrud.git
cd usuarios-crud
```

Segundo paso: intalar la dependencia

```sh
npm  install
```

Terce paso ;: configuar Mysql; Si la base de datos aún no existe, créala manualmente ejecutando:

```sql
CREATE DATABASE usuario_crud;
USE usuario_crud;

CREATE TABLE usuario (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    edad INT NOT NULL
);

```

Cuarto paso; configurar la conexion  a la base de datos 
 Asegúrate de configurar correctamente la conexión en LoopBack. Revisa el archivo src/datasources/mysql.datasource.ts y ajusta los valores según tu configuración:
```ts
const config = {
  name: 'mysql',
  connector: 'mysql',
  url: '',
  host: 'localhost',
  port: 3306,
  user: 'root',// Cambia esto si usas otro usuario
  password: '',  // Ingresa tu contraseña de MySQL si es necesario
  database: 'usuario_crud'
};
 ```
Quinto Paso :Ejecutas  la aplicacion :
```sh
npm start
 ```
La API estará disponible en http://127.0.0.1:3000/

Sexto paso:PRUEBAS DE LA API
Obtener los Usuarios
```nginx
GET http://127.0.0.1:3000/usuarios


 ```
 Crear un usuario (POST en Postman) de esta forma  pruebas   "con GET, POST , DELETE , PUT "

```json

{
  "nombre": "Carlos Gómez",
  "email": "carlos@gmail.com",
  "edad": 28
}

```
Actualziar un Usuario
 ```

PUT http://127.0.0.1:3000/usuarios/1

```
Elimianr usuario
 ```

DELETE http://127.0.0.1:3000/usuarios/1

```





```

