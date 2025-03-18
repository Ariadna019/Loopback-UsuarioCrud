# usuarios-crud

LoopBack CRUD con MySQL
Este proyecto es una API REST creada con LoopBack que permite gestionar información a través de un CRUD (Create, Read, Update, Delete). Se conecta con una base de datos MySQL y permite interactuar con la información mediante Postman o directamente con LoopBack Explorer.



Configuración de la Base de Datos
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

