# Proyecto 1: Desarrollando una aplicación web: De la teoría a la práctica

## Documento de propuesta

### Nombre del proyecto: Gestor de portafolios

---

### Descripción del proyecto

La idea del proyecto es la realización de una página web que permita a los usuarios registrarse en una plataforma administrativa donde puedan añadir información propia para rellenar los datos de un portafolio / Currículum Vitae en línea; una vez añadida toda la información (mediante un acceso privado de cada usuario), se generará una dirección URL donde se podrá encontrar el portafolio creado y será accesible por todo el público.

---

### Público objetivo

El público objetivo principalmente serán personas no asociadas al mundo de la programación y que tengan capacidad para mostrar proyectos que hayan realizado, por ejemplo: diseñadores gráficos, caracterizadores, investigadores, etc.
A su vez, también podrían llegar a utilizar el proyecto personas asociadas al mundo de la programación recién graduadas que todavía no tienen demasiados conocimientos como para poder generar su propio portafolio o que no quieren pararse a realizar el desarrollo del mismo.

---

### Análisis de mercado

Actualmente, los principales competidores serían los distintos portales de empleo, debido a que tienen un apartado en el que los usuarios pueden crear su propio perfil público enfocado al mundo laboral; sin embargo, esas plataformas (como pueden ser LinkedIn, InfoJobs, TecnoEmpleo, Indeed, etc), están más enfocados a que el perfil se desarrolle de una forma más directa con poca customización debido a que realmente se tratan más de redes sociales más que de enseñar lo que puedes realizar.

Por ello, lo que diferencia realmente a mi proyecto frente a la competencia es esa capacidad de customización prácticamente completa y la comodidad de que sin necesidad de saber programar, puedes terminar teniendo una dirección URL mediante la cual, puedes enseñar todos los datos que quieras y lo más importante, lo que eres capaz de hacer, al gusto estético que el usuario quiera tener.
Además, el proyecto sirve también como fuente de investigación para el sector de Recursos Humanos, ya que los distintos portafolios que se generen a través de la plataforma, se podrá ver el resultado visual de los mismos de todos los usuarios de la plataforma.

---

### Funcionalidades claves

#### 1. Gestión de Usuarios

- Inicio de Sesión: Los usuarios pueden iniciar sesión en la plataforma con credenciales creadas mediante una pantalla de registro.
- Perfil de Usuario: Cada usuario tiene un perfil que incluye información como nombre completo, correo electrónico, número de teléfono (opcional), país, redes sociales, imagen de perfil, y CV (subido a través de Cloudinary).
- Idiomas: Los usuarios pueden agregar y gestionar los idiomas que dominan, incluyendo el nombre del idioma y el nivel de fluidez.
- Edición de Perfil: Los usuarios pueden editar su perfil, excepto el rol y el estado de la cuenta.
- Redes Sociales: Los usuarios pueden añadir y gestionar los enlaces a sus perfiles de redes sociales.
- Gestión de Administradores: Los administradores pueden gestionar los roles de los diversos usuarios y eliminar un portafolio o cuenta de usuario en caso de que se detecte mal uso de la plataforma.

#### 2. Gestión de Portafolios

- Creación de Portafolios: Los usuarios autenticados pueden crear un portafolio para mostrar su información profesional.
- Personalización del Portafolio: Los usuarios pueden personalizar las secciones y subsecciones del portafolio, como el color de fondo, títulos de presentación, servicios ofrecidos, y el contenido de cada sección.
- Slug Único: Cada portafolio tiene un slug único que permite a los usuarios acceder a su portafolio mediante una URL personalizada.
- Visualización Pública: Los portafolios son visibles públicamente por cualquier visitante a través del slug o el id del portafolio.

#### 3. Secciones del Portafolio

- Sección Principal (Home Section): Incluye un título de presentación y un subtítulo con el cargo actual del usuario, acompañado de un fondo personalizable.
- Sección de Servicios (Services Section): Los usuarios pueden listar y gestionar los servicios o especialidades que ofrecen.
- Sección "Sobre Mí" (About Section): Incluye un título de presentación, una frase sobre el tiempo de experiencia laboral y un contenido personalizado donde el usuario puede describirse.
- Sección de Resumen (Resume Section):
  - Sobre Mí (About Me): Contiene un resumen de la experiencia profesional del usuario y los años de experiencia.
  - Experiencia Profesional: Los usuarios pueden añadir múltiples experiencias laborales, con detalles como fechas de inicio y fin, el nombre de la empresa y el cargo ocupado.
  - Educación: Los usuarios pueden agregar sus estudios, con información como fechas, nombre del curso, institución educativa y horas dedicadas al curso.
  - Habilidades: Los usuarios pueden listar sus habilidades profesionales.
  - Secciones Adicionales: Los usuarios pueden agregar secciones personalizadas (e.g., proyectos, certificados, logros, voluntariado), cada una con su propio fondo y contenido.

#### 4. Gestión de Archivos

- Subida de Imágenes: Los usuarios pueden subir su imagen de perfil a través de Cloudinary y mostrarla en el portafolio.
- Subida de CV: Los usuarios pueden subir su CV en formato PDF a través de Cloudinary para que esté disponible para descarga pública desde el portafolio.

#### 5. Funcionalidades de Administración

- Control de Acceso: Los administradores son responsables de gestionar las cuentas de usuario.
- Gestión de Roles: Los administradores tienen privilegios especiales para gestionar los usuarios, mientras que los usuarios estándar pueden gestionar solo su información.

#### 6. Visualización Pública de Portafolios

- Portafolios de Prueba: La plataforma ofrece varios portafolios de prueba visibles para los visitantes, que muestran ejemplos de las funcionalidades que se pueden utilizar.
- Acceso a Portafolios: Los visitantes pueden acceder a cualquier portafolio público mediante su slug o id.

#### 7. Seguridad y Privacidad

- Autenticación: Uso de JSON Web Tokens (JWT) o sesiones seguras para gestionar el inicio de sesión de los usuarios.
- Autorización: Control estricto de acceso para proteger las funcionalidades de edición de portafolio y administración.
- Protección de Datos: Validación de los datos introducidos por los usuarios.

#### 8. Multilenguaje

- Gestión de Idiomas: Los usuarios pueden desarrollar el portafolio en todos los idiomas que los usuarios deseen, otorgando las traducciones correspondientes.

---

### Tecnologías seleccionadas

| Categoría            | Tecnología seleccionada |
| -------------------- | ----------------------- |
| Base de datos        | MongoDB                 |
| Backend              | Express.js              |
| Frontend             | Angular                 |
| Entorno de ejecución | Node.js                 |

#### Justificaciones de las tecnologías utilizadas

He decidido utilizar el **stack MEAN**, que es un conjunto de marcos de desarrollo y tecnologías utilizadas par el desarrollo web de aplicaciones. Este conjunto está conformado por las tecnologías mostradas en la tabla superior del apartado **"Tecnologías seleccionadas"**.

El **stack MEAN** es un conjunto extremadamente versátil, con alta capacidad de documentación y ejemplos, además de una gran comunidad de programadores con distintas plataformas disponibles para ver código de otros programadores. Las tecnologías empleadas a su vez van actualizándose períodicamente. Una de esas plataformas es: [Stack Overflow](https://stackoverflow.com/)

Los principales motivos por los cuales he seleccionado este stack son los siguientes:

- Abarcar todo el ciclo de desarrollo, desde frontend hasta backend.
- Facilitar el trabajo al usar una arquitectura modelo vista controlador (MVC).
- Aportar un conjunto de librerías que permiten agilizar el trabajo pesado innecesario.
- Basarse en tecnologías altamente conocidas, utilizadas, actualizadas y respaldadas por la comunidad.
- Utilización de un único lenguaje de programación, ejecutado en todos los niveles de la aplicación.
- Frameworks basados en código abierto.

Al hablar sobre el **stack MEAN** se suele comparar con el **stack MERN**, cuya única diferencia es el uso de Angular o React, respectivamente. En este caso, la decisión tomada para usar Angular frente a React es debida por la superioridad de conocimientos adquiridos de Angular del alumno en la actualidad.

> Referencias: [MERN Stack: Qué es y qué ventajas ofrece | OpenWebinars](https://openwebinars.net/blog/mern-stack-que-es-y-que-ventajas-ofrece/)
