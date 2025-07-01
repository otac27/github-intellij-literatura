README.
📚 Literatura App

Aplicación de consola desarrollada en Java con Spring Boot que permite importar y gestionar libros y autores desde la API pública de [Gutendex](https://gutendex.com/). Utiliza PostgreSQL para almacenamiento de datos y está diseñada siguiendo buenas prácticas para facilitar su escalabilidad y mantenimiento.

## 🚀 Funcionalidades

- ✅ Buscar libros por título  
- 📖 Listar libros registrados con su autor  
- 👤 Listar autores registrados  
- 🟢 Listar autores vivos  
- 🌍 Listar libros por idioma  
- 🔄 Importar libros desde la API de Gutendex (evitando duplicados)  

## 🛠️ Tecnologías utilizadas

- Java 21  
- Spring Boot 3.5  
- Spring Data JPA  
- PostgreSQL  
- Hibernate ORM  
- Maven  

## 🧠 Estructura del proyecto


src/
 ├── main/
 │ ├── java/
 │ │ └── com.maos.literatura/
 │ │ ├── modelo/ → Entidades Autor y Libro
 │ │ ├── dto/ → DTOs usados para la API Gutendex
 │ │ ├── repositorio/ → Repositorios JPA
 │ │ ├── servicio/ → Servicio que consume la API externa
 │ │ └── LiteraturaApplication.java → Lógica principal con menú interactivo
 │ └── resources/
 │ └── application.properties → Configuración de la base de datos

## ⚙️ Configuración inicial

1. Clona el repositorio:

```bash
git clone https://github.com/tu-usuario/literatura-app.git
cd literatura-app

Crea la base de datos PostgreSQL:


CREATE DATABASE literatura;

Configura las credenciales en src/main/resources/application.properties:


spring.datasource.url=jdbc:postgresql://localhost:5432/literatura
spring.datasource.username=postgres
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update

Ejecuta el proyecto:


mvn spring-boot:run

🎯 Ejemplo de uso
Cuando ejecutes la aplicación, verás un menú interactivo como este:
Elija una opción:
1 - Buscar libro por título
2 - Listar libros registrados
3 - Listar autores registrados
4 - Listar autores vivos
5 - Listar libros por idioma
6 - Importar libros desde la API de Gutendex
0 - Salir

🤝 Contribuciones
Las contribuciones son bienvenidas. Si tienes sugerencias o deseas mejorar alguna funcionalidad, no dudes en abrir un issue o enviar un pull request.

🎓 Proyecto desarrollado como parte de un challenge técnico de práctica con Java y Spring Boot.


