# API de Usuarios

## Resumen

Esta API facilita la administración de usuarios mediante operaciones CRUD, desarrollada con .NET 8 y SQL Server. Se implementa el patrón Repository y se documenta con Swagger.

## Requisitos del Entorno

- Visual Studio 2022 o posterior
- .NET 8 o superior
- SQL Server

## Características de la API

La API gestiona una entidad denominada **Usuario**, que incluye los siguientes atributos:

- **Id** (int): Identificador único, autoincremental.
- **Nombre** (string): Campo obligatorio, máximo 100 caracteres.
- **Correo** (string): Requerido, debe ser un correo electrónico válido.
- **Edad** (int): Campo obligatorio, debe ser mayor a 0.

## Puntos de Acceso (Endpoints)

### Listar todos los usuarios

`GET /api/usuarios`

- **Descripción**: Retorna el conjunto de usuarios registrados.

### Consultar un usuario por ID

`GET /api/usuarios/{id}`

- **Descripción**: Proporciona los detalles de un usuario específico.

### Registrar un nuevo usuario

`POST /api/usuarios`

- **Descripción**: Agrega un usuario a la base de datos.

### Actualizar un usuario

`PUT /api/usuarios/{id}`

- **Descripción**: Modifica la información de un usuario existente.

### Eliminar un usuario

`DELETE /api/usuarios/{id}`

- **Descripción**: Remueve un usuario de la base de datos.

## Gestión de Datos

Se emplea **Entity Framework Core** y **SQL Server** para el almacenamiento de datos.

## Buenas Prácticas Implementadas

- Aplicación del **patrón Repository** para desacoplar el acceso a datos.
- Manejo estructurado de **excepciones**, con respuestas HTTP adecuadas.
- **Documentación** mediante **Swagger** para mejorar la usabilidad.

## Instalación y Configuración

### Clonar el Repositorio

```sh
 git clone <URL_DEL_REPOSITORIO>
```

### Ajustar la conexión a la base de datos en `appsettings.json`

### Aplicar las migraciones

```sh
 dotnet ef database update
```

### Compilar y ejecutar la API

```sh
 dotnet run
```

### Link del documento de los pasos del uso de la API

```sh
 https://docs.google.com/document/d/1y9LAlvl6DFEVtk0Ut2T8OO3EW6OHNdrrgYqDcE20_40/edit?usp=sharing
```

---

Creado por Jonathan Alexander Tejada Jiménez
