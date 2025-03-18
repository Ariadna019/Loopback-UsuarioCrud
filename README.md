# usuarios-crud

LoopBack CRUD con MySQL
Este proyecto es una API REST creada con LoopBack que permite gestionar información a través de un CRUD (Create, Read, Update, Delete). Se conecta con una base de datos MySQL y permite interactuar con la información mediante Postman o directamente con LoopBack Explorer.

-Conexión con MySQL.
-CRUD de usuarios (crear, leer, actualizar y eliminar).
-Interfaz gráfica proporcionada por LoopBack Explorer.
-Posibilidad de probar los endpoints en Postman.

## Install dependencies

```sh
npm install
```

To only install resolved dependencies in `package-lock.json`:

```sh
npm ci
```

## Run the application

```sh
npm start
```

You can also run `node .` to skip the build step.

Open http://127.0.0.1:3000 in your browser.

## Rebuild the project

To incrementally build the project:

```sh
npm run build
```

La base de datos usando para el proeycto  es llamndo usuario-crud, con la tabla usuario, siendo esta la estructura:
CREATE TABLE usuario (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    edad INT NOT NULL
);

