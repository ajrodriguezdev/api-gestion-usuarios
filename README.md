# 🚀 API REST - Gestión de Usuarios

<p align="center">
  <img src="https://img.shields.io/badge/Java-17%2B-orange?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java"/>
  <img src="https://img.shields.io/badge/Spring_Boot-Backend-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot"/>
  <img src="https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Maven-Build-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white" alt="Maven"/>
</p>

<p align="center">
  API REST para la administración de usuarios, autenticación y control de acceso, desarrollada con Java y Spring Boot siguiendo una arquitectura por capas y buenas prácticas de desarrollo backend.
</p>

---

## 📌 Descripción del proyecto

**API REST - Gestión de Usuarios** es un proyecto backend diseñado para centralizar y administrar la información de usuarios mediante servicios REST.

El sistema permitirá realizar operaciones CRUD, gestionar credenciales, autenticar usuarios y proteger los recursos mediante mecanismos de seguridad.

El desarrollo está orientado a implementar una arquitectura organizada, mantenible y escalable, separando las responsabilidades de cada componente de la aplicación.

## 🎯 Objetivos

- Desarrollar servicios REST utilizando Java y Spring Boot.
- Implementar operaciones CRUD para la gestión de usuarios.
- Diseñar e integrar una base de datos relacional con PostgreSQL.
- Aplicar una arquitectura por capas.
- Implementar autenticación y autorización.
- Gestionar excepciones y validaciones.
- Documentar y probar los endpoints de la API.

## ⚙️ Funcionalidades

| Funcionalidad | Descripción | Estado |
|---|---|---|
| Registro de usuarios | Crear nuevos usuarios con validación de información | 📋 Pendiente |
| Consulta de usuarios | Consultar usuarios individualmente o mediante listados | 📋 Pendiente |
| Actualización de usuarios | Modificar información de usuarios existentes | 📋 Pendiente |
| Eliminación de usuarios | Eliminar registros de usuarios | 📋 Pendiente |
| Autenticación | Validar credenciales para iniciar sesión | 📋 Pendiente |
| Seguridad | Proteger endpoints y controlar permisos | 📋 Pendiente |
| Validaciones | Validar datos de entrada y reglas de negocio | 📋 Pendiente |
| Manejo de excepciones | Gestionar errores mediante respuestas HTTP adecuadas | 📋 Pendiente |

## 🛠️ Tecnologías utilizadas

### Backend
- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- Spring Security
- Hibernate

### Base de datos
- PostgreSQL
- SQL

### Herramientas
- Maven
- Git y GitHub
- Postman
- IntelliJ IDEA o Visual Studio Code

## 🏗️ Arquitectura del proyecto

El proyecto utilizará una arquitectura por capas para separar responsabilidades y facilitar el mantenimiento del código.

```text
src/
└── main/
    ├── java/
    │   └── com/
    │       └── gestionusuarios/
    │           ├── controller/
    │           ├── service/
    │           ├── repository/
    │           ├── entity/
    │           ├── dto/
    │           ├── security/
    │           ├── exception/
    │           └── GestionUsuariosApplication.java
    │
    └── resources/
        └── application.properties
```

### Responsabilidad de cada capa

| Capa | Responsabilidad |
|---|---|
| Controller | Recibir solicitudes HTTP y exponer los endpoints REST |
| Service | Implementar la lógica de negocio |
| Repository | Gestionar el acceso y las operaciones con la base de datos |
| Entity | Representar las entidades del modelo de datos |
| DTO | Controlar la información que entra y sale de la API |
| Security | Gestionar autenticación y autorización |
| Exception | Centralizar el manejo de errores |

## 🔗 Endpoints proyectados

Los siguientes endpoints representan el diseño inicial de la API. Se actualizarán cuando sean implementados.

| Método | Endpoint | Descripción |
|---|---|---|
| POST | `/api/auth/register` | Registrar un usuario |
| POST | `/api/auth/login` | Iniciar sesión |
| GET | `/api/users` | Consultar todos los usuarios |
| GET | `/api/users/{id}` | Consultar un usuario por ID |
| PUT | `/api/users/{id}` | Actualizar un usuario |
| DELETE | `/api/users/{id}` | Eliminar un usuario |

## 🗄️ Modelo de datos

La entidad principal será `User`, que almacenará la información necesaria para identificar y administrar cada usuario.

| Campo | Tipo de dato | Descripción |
|---|---|---|
| id | Long | Identificador único |
| name | String | Nombre del usuario |
| email | String | Correo electrónico |
| password | String | Contraseña almacenada de forma segura |
| role | String / Enum | Rol asignado al usuario |
| createdAt | LocalDateTime | Fecha de creación |

*El modelo podrá evolucionar durante el desarrollo.*

## 🔐 Seguridad

Se contempla implementar mecanismos para proteger la información y controlar el acceso a los recursos:

- Cifrado de contraseñas.
- Autenticación de usuarios.
- Autorización basada en roles.
- Validación de solicitudes.
- Protección de endpoints privados.
- Manejo seguro de credenciales y variables de entorno.

## 🚀 Instalación y ejecución

### Requisitos previos

- Java 17 o superior.
- Maven.
- PostgreSQL.
- Git.

### 1. Clonar el repositorio

```bash
git clone https://github.com/ajrodriguezdev/api-gestion-usuarios.git
```

### 2. Ingresar al proyecto

```bash
cd api-gestion-usuarios
```

### 3. Configurar la base de datos

Crear una base de datos en PostgreSQL y configurar las credenciales de conexión en `application.properties`.

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/gestion_usuarios
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 4. Ejecutar la aplicación

```bash
mvn spring-boot:run
```

*Las instrucciones definitivas se completarán cuando la aplicación esté implementada.*

## 🧪 Pruebas

Se utilizará Postman para verificar el comportamiento de los endpoints, validar respuestas HTTP y comprobar las operaciones CRUD, autenticación y manejo de errores.

## 🗺️ Roadmap

- [ ] Configuración inicial de Spring Boot y Maven.
- [ ] Conexión con PostgreSQL.
- [ ] Creación de entidades y repositorios.
- [ ] Implementación de DTO y validaciones.
- [ ] Desarrollo de operaciones CRUD.
- [ ] Implementación de la capa de servicios.
- [ ] Autenticación y autorización con Spring Security.
- [ ] Manejo global de excepciones.
- [ ] Pruebas de endpoints con Postman.
- [ ] Documentación de la API.
- [ ] Pruebas automatizadas.

## 👩‍💻 Autora

**Andrea Rodriguez**

Ingeniera de Sistemas | Backend Developer

- GitHub: [@ajrodriguezdev](https://github.com/ajrodriguezdev)
- LinkedIn: [Perfil profesional](https://www.linkedin.com/in/aj-rodriguez-g)

---

<p align="center">
  Proyecto desarrollado con Java y Spring Boot.
  <br/>
  <b>Construyendo soluciones backend, una API a la vez. 💻</b>
</p>
