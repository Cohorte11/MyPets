# Ejercicio Grupal “MyPets” pt 3: Filtros de Búsqueda con JPQL y Seguridad Básica
En esta tercera parte del ejercicio, añadirás filtros de búsqueda a tus entidades usando JPQL y protegerás algunas rutas con seguridad básica usando Spring Security.

## Instrucciones del Ejercicio
1. Añadir Filtros de Búsqueda con JPQL en los Repositorios
  - Define métodos en los repositorios de tus entidades (User, PetProfile, Post, Comment, Like) que utilicen JPQL para realizar búsquedas avanzadas.
  - Implementa métodos para búsquedas por nombre, fecha de creación, y otros atributos relevantes de tus entidades.
2. Implementar Seguridad Básica en Controladores
  - Configura Spring Security para proteger ciertos endpoints de tu aplicación, asegurándote de que solo los usuarios autenticados puedan acceder a ellos.
  - Añade roles de usuario (por ejemplo, ADMIN y USER) y asegúrate de que solo los usuarios con el rol adecuado puedan acceder a ciertos endpoints.
3. Actualizar Controladores para Utilizar Filtros de Búsqueda y Seguridad
  - Modifica los controladores para incluir endpoints que utilicen los filtros de búsqueda definidos en los repositorios.
  - Asegúrate de que los controladores manejen correctamente la seguridad configurada.
4. Probar la API con Postman
  - Utiliza Postman para probar los nuevos endpoints y asegurarte de que los filtros de búsqueda funcionan correctamente.
  - Verifica que los endpoints protegidos requieran autenticación y autorización apropiadas.
  - Prueba la seguridad enviando solicitudes con diferentes credenciales y verificando que se apliquen las restricciones de acceso adecuadamente.


# Ejercicio individual "Ecommerce"
Este ejercicio consiste en la creación de una API REST para un e-commerce básico. El objetivo es implementar las entidades Categoria, ECategoria, Rol, ERol, Usuario y Producto, y desarrollar la lógica completa de la aplicación usando Spring Boot. Posteriormente, esta API se utilizará para el desarrollo de una aplicación frontend con React.

## Instrucciones del Ejercicio
1. Configuración Inicial del Proyecto
  - Crear un nuevo proyecto Spring Boot:
  - Utiliza Spring Initializr para crear un nuevo proyecto con las siguientes dependencias: Spring Web, Spring Data JPA, Spring Security, MySQL Driver, y Spring Boot DevTools.

2. Configurar el archivo application.properties:
  - Configura las propiedades de conexión a la base de datos MySQL.

2. Definir las Entidades
  - Categoria y ECategoria:
    - Define la entidad Categoria con los campos necesarios y la enumeración ECategoria con los valores HOMBRES, MUJERES, NINOS.
   
  - Rol y ERol:
    - Define la entidad Rol con los campos necesarios y la enumeración ERol con los valores USER y ADMIN.
   
  - Usuario:
    - Define la entidad Usuario que tenga relación con la entidad Rol. Incluye campos como nombre, apellido, correo, password.
   
  - Producto:
    - Define la entidad Producto con campos como nombreProducto, stockProducto, precioProducto, y una relación con la entidad Categoria.
   
3. Crear los Repositorios
  - Definir interfaces de repositorios:
  - Crea interfaces en el paquete com.ecommerce.repository para cada entidad (Categoria, Rol, Usuario, Producto) extendiendo JpaRepository.

4. Implementar los Servicios
  - Crear servicios para las entidades que lo necesiten:
  - Crea clases de servicio en el paquete com.ecommerce.service que implementen la lógica de negocio para las entidades necesarias.
  - Inyecta los repositorios en los servicios usando @Autowired.

5. Desarrollar los Controladores REST
  - Crear controladores para las entidades:
  - Define clases de controlador en el paquete com.ecommerce.controller para manejar las solicitudes HTTP para las entidades (Usuario, Producto).
  - Utiliza los servicios dentro de los controladores para realizar las operaciones CRUD (Crear, Leer, Actualizar, Eliminar).
  - Implementa métodos en los controladores para manejar las rutas necesarias (/api/categorias, /api/usuarios, /api/productos).

6. Proteger la API con Spring Security
  - Configurar Spring Security:
  - Configura la clase de seguridad para proteger los endpoints.
  - Define la configuración de seguridad básica para manejar autenticación y autorización.

7. Probar la API con Postman
  - Utilizar Postman para probar los endpoints:
  - Realiza operaciones CRUD para verificar que todos los endpoints funcionen correctamente.
  - Prueba la autenticación y autorización enviando solicitudes a los endpoints protegidos.
  - Verifica que las respuestas sean adecuadas y manejen correctamente los errores.
    
