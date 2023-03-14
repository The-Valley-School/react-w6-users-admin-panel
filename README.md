# WORKSHOP 6 - Panel de admin de usuarios

En este workshop vamos a realizar la siguiente página:

![home.png](/assets/home.png)

Como puedes observar en la parte de arriba hay una cabecera que nos permite cambiar de idioma entre Español e Inglés:

![home-eng.png](/assets/home-eng.png)

**Traducciones**

Para las traducciones te dejamos los JSONs por aquí:

en.json

```json
{
  "header.logo": "Users!",
  "header.home": "Home",
  "header.users": "Users",
  "header.createUser": "Create User",
  "header.spanish": "ES",
  "header.english": "EN",
  "users:title": "Users",
  "users:loading": "Loading...",
  "users:name": "Name",
  "users:username": "Username",
  "users:email": "Email",
  "users:website": "Website",
  "home:welcome": "Welcome!",
  "home:userManagement": "This is a user management application",
  "home:apiDisclaimer": "On this website, you can store as many users as you want, but remember that they will not be saved in the API... sorry :(",
  "createUserPage.title": "Create User",
  "createUserPage.name": "Name:",
  "createUserPage.username": "Username:",
  "createUserPage.email": "Email:",
  "createUserPage.phone": "Phone:",
  "createUserPage.website": "Website:",
  "createUserPage.required": "This field is required",
  "createUserPage.submitButton": "Create User",
  "createUserPage.error": "Error creating user"
}
```

es.json

```json
{
  "header.logo": "¡Usuarios!",
  "header.home": "Inicio",
  "header.users": "Usuarios",
  "header.createUser": "Crear usuario",
  "header.spanish": "ES",
  "header.english": "EN",
  "users:title": "Usuarios",
  "users:loading": "Cargando...",
  "users:name": "Nombre",
  "users:username": "Nombre de usuario",
  "users:email": "Correo electrónico",
  "users:website": "Sitio web",
  "home:welcome": "¡Bienvenido!",
  "home:userManagement": "Esta es una aplicación de gestión de usuarios",
  "home:apiDisclaimer": "En esta web podrás almacenar los usuarios que quieras, pero recuerda que no se guardarán en el API... lo siento :(",
  "createUserPage.title": "Crear Usuario",
  "createUserPage.name": "Nombre:",
  "createUserPage.username": "Nombre de usuario:",
  "createUserPage.email": "Correo electrónico:",
  "createUserPage.phone": "Teléfono:",
  "createUserPage.website": "Sitio web:",
  "createUserPage.required": "Este campo es obligatorio",
  "createUserPage.submitButton": "Crear Usuario",
  "createUserPage.error": "Error al crear el usuario"
}
```

**Lista de usuarios**

En cuanto a las páginas, encontrarás /users con la lista de usuarios:

![users.png](/assets/users.png)

Dichos usuarios deberán venir de la API:

<https://jsonplaceholder.typicode.com/users>

Esa URL deberás guardarla en un fichero privado .env.local y la página también se deberá poder traducir al inglés.

**Creación de usuarios**

Por otro lado encontrarás la página /create-user donde podrás crear un usuario: 

![create-user.png](/assets/create-user.png)

Este formulario debe estar creado con React-hook-forms y los campos deben ser obligatorios:

![create-user-error.png](/assets/create-user-error.png)

Para añadir un usuario haremos una petición POST a la misma API:

<https://jsonplaceholder.typicode.com/users>

Ten en cuenta que aunque la API responda 200, luego al pedir los usuarios no devolverá el nuevo usuario (es una API fake). Si la creación del usuario ha devuelto 200 navegaremos a la página del listado de nuevo (/users) 

**Router**

Deberás usar el HashRouter para que cuando despleguemos nuestra app no tengamos problemas

**Testing**

Debes realizar testing unitarios para los componentes:

- HomePage
- Cabecera

Si te da tiempo también añade tests para:

- CreateUserPage
- UsersPage

**ESLint, Prettier y Husky**

Debes instalar y configurar ESLint para que la aplicación pase ciertas reglas de lintado, antes de comitear Husky debe obligarnos a que el linter y los tests estén OK.

Configura también prettier para poder formatear el código a tu gusto.

**Despliegue**

Cuando termines debes desplegar tu App en Netlify

<https://www.netlify.com/>