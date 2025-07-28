
# Go Clean Template - Task Management API

## Descripción

Go Clean Template tiene el objetivo de mostrar buenas prácticas de arquitectura limpia en el desarrollo de APIs RESTful utilizando Go. Esta versión personalizada incluye una implementación CRUD para una entidad `Task`, así como un endpoint adicional para listar tareas completadas.

El código no tiene fines comerciales.

---

## Arquitectura

El proyecto sigue los principios de **Clean Architecture**, y está organizado en capas:

- **Entity**: Define estructuras del dominio (`Task`).
- **Repository**: Interfaces y su implementación para persistencia (PostgreSQL).
- **Usecase**: Lógica de negocio.
- **Delivery**: Comunicación HTTP utilizando Gin.
- **Config**: Configuración de entorno y conexión a base de datos.
- **Main**: Inicialización de dependencias y ejecución del servidor.

---

## Tecnologías utilizadas

- [Golang](https://golang.org/)
- [Gin](https://github.com/gin-gonic/gin)
- [PostgreSQL](https://www.postgresql.org/)
- [database/sql](https://pkg.go.dev/database/sql)
- [uuid](https://github.com/google/uuid)

---

## Características

- CRUD completo para la entidad `Task` (`Create`, `Read`, `Update`, `Delete`).
- Endpoint adicional para filtrar tareas completadas.
- Uso de UUID como identificador único.
- Validaciones básicas en los handlers.
- Configuración mediante variables de entorno.
- Migración SQL simple para la tabla `tasks`.

---

📌 Endpoints Disponibles
Método	Ruta	Descripción
POST	/tasks	Crear nueva tarea
GET	/tasks	Listar todas las tareas
GET	/tasks/completed	Listar tareas completadas
GET	/tasks/:id	Obtener tarea por ID
PUT	/tasks/:id	Actualizar tarea por ID
DELETE	/tasks/:id	Eliminar tarea por ID

Ejemplo de creación de tarea:
```bash

POST /tasks
Content-Type: application/json

{
  "title": "Terminar el README",
  "completed": false
}
```

Respuesta:

```bash
{
  "id": "9a36f415-8398-4e77-875d-4a32c7fa2fbd",
  "title": "Terminar el README",
  "completed": false
}
```

## 🚀 Deploy en Railway
Este proyecto puede desplegarse fácilmente en plataformas como Railway:

Crear un nuevo proyecto y conectar con GitHub.

Añadir el plugin de PostgreSQL.

Configurar las variables DATABASE_URL y SERVER_ADDRESS.

Hacer push para activar el deploy automático.

## 📝 Créditos y licencia
Este proyecto fue adaptado a partir de:

Repositorio original: evrone/go-clean-template

Licencia original: MIT License

El código fue modificado con fines educativos y de demostración técnica, sin fines comerciales.

## Desarrollado con ❤️ por spookycoincidence
