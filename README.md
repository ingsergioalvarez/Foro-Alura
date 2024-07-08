Sistema de Foro Challenge - Documentación
Este proyecto es un sistema de foro que permite la autenticación de usuarios, creación de usuarios, publicación de mensajes en un foro y respuestas a comentarios dentro del foro. Utiliza Spring Boot y está conectado a una base de datos MySQL.

Configuraciones
Perfiles Activos
El proyecto soporta los siguientes perfiles activos:

dev: Configuración de desarrollo.
test: Configuración para pruebas.
prod: Configuración para producción.
El perfil activo se puede cambiar en el archivo de configuración application.properties.

Base de Datos
MySQL
El proyecto utiliza MySQL como base de datos. A continuación se muestra la configuración para la base de datos:

datasource.url=jdbc:mysql://localhost/foro_Challenge?createDatabaseIfNotExist=true&serverTimezone=UTC
datasource.username=root
datasource.password=123456

JPA
Se utiliza JPA con las siguientes configuraciones:
jpa.show-sql=true
hibernate.format_sql=true
Esto habilita la visualización de consultas SQL generadas y formatea las consultas para una mejor legibilidad.

Servidor
El servidor está configurado para ejecutarse en el puerto 8081.
server.port=8081

Seguridad
La seguridad del API utiliza un secreto JWT para la autenticación:
api.security.secret=${JWT_SECRET:123456}

Controladores
El proyecto incluye los siguientes controladores:

LoginController: Autenticación de usuarios.
UsuarioController: Creación de usuarios.
MensajeController: Creación de mensajes en el foro.
ComentarioController: Respuestas a comentarios dentro del foro.
Ejecución del Proyecto
Para ejecutar el proyecto localmente:

Asegúrate de tener configurada una instancia de MySQL en tu máquina local.
Configura las credenciales de acceso a MySQL en el archivo application.properties.
Ejecuta la aplicación Spring Boot desde tu IDE o mediante el comando mvn spring-boot:run.
