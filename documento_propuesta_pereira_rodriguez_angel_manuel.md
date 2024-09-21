# Proyecto 1: Desarrollando una aplicación web: De la teoría a la práctica

## Documento de propuesta

### Nombre del proyecto: Gestor de portafolios

---

### Descripción del proyecto

La idea del proyecto es la realización de una página web que permita a los usuarios registrarse en una plataforma administrativa donde puedan añadir información propia para rellenar los datos de un **portafolio** / **Currículum Vitae en línea**; una vez añadida toda la información (mediante un acceso privado de cada usuario), se generará una **dirección URL** donde se podrá encontrar el portafolio creado y será accesible por todo el **público**.

---

### Público objetivo

El proyecto está dirigido a profesionales de diversos sectores que necesitan una plataforma **eficiente** y **fácil de usar** para mostrar su trayectoria. Los segmentos clave incluyen:

- **Freelancers**: Profesionales independientes que buscan atraer clientes o proyectos mediante un portfolio visual y completo.
- **Desarrolladores y Creativos**: Programadores, diseñadores, fotógrafos y otros creativos que quieren destacar su trabajo y experiencia de forma organizada.
- **Estudiantes y recién graduados**: Usuarios que buscan su primer empleo y necesitan una plataforma que les permita mostrar sus proyectos académicos y habilidades adquiridas.

---

### Análisis de mercado

#### Contexto del Mercado

El mercado de las plataformas de portafolios digitales ha **crecido significativamente** en los últimos años, impulsado por la **creciente demanda** de profesionales que buscan una **forma eficaz** de mostrar sus habilidades y experiencia en línea. Esta demanda proviene de una **variedad de sectores** como el diseño gráfico, la programación, la escritura, y la consultoría, donde los portafolios sirven como una **herramienta clave** para atraer clientes, empleadores o colaboradores. El crecimiento de la gig economy y el trabajo remoto ha intensificado la **necesidad de soluciones accesibles** para gestionar portafolios.

#### Competencia

Existen varias plataformas que permiten a los profesionales crear y gestionar portafolios en línea, algunas de las más destacadas incluyen:

- **Behance**: Centrada en creativos (diseñadores, fotógrafos, artistas), ofrece una interfaz muy visual y acceso a una comunidad global.
- **Dribbble**: Similar a Behance, pero más orientada a diseñadores gráficos y desarrolladores UI/UX.
- **LinkedIn**: Aunque no es una plataforma de portafolios tradicional, permite a los profesionales mostrar su experiencia y proyectos en un perfil público ampliamente utilizado.
- **WordPress/Wix**: Plataformas de creación de sitios web que ofrecen plantillas para portafolios personalizados, permitiendo flexibilidad y control total.

#### Ventajas Competitivas del Proyecto

Este gestor de portafolios se diferenciaría en varios aspectos:

- **Personalización flexible**: Permite a los usuarios personalizar múltiples secciones y subsecciones, algo que las plataformas como Behance o LinkedIn no permiten en detalle.
- **Simplicidad de uso**: A diferencia de soluciones como WordPress o Wix, el proyecto está orientado a usuarios que buscan una plataforma más específica y rápida de implementar, sin la complejidad de construir un sitio web completo.
- **Gestión centralizada**: Se integran herramientas como la subida de imágenes y CV a través de Cloudinary, lo que simplifica la gestión de archivos multimedia.

#### Oportunidades de Crecimiento

- **Expansión multisectorial**: Puede expandirse para atender a más sectores profesionales, como escritores, consultores o incluso empresas que desean mostrar su trabajo a través de portafolios corporativos.
- **Funcionalidades avanzadas**: La integración de características adicionales como analítica del portafolio (para ver quién lo visita), plantillas prediseñadas o integración con redes sociales profesionales podría atraer más usuarios.

#### Riesgos y Desafíos

- **Competencia establecida**: Competir con plataformas ya consolidadas como Behance y Dribbble puede ser un reto debido a la gran base de usuarios y recursos que ya poseen.
- **Diferenciación de valor**: Será esencial posicionarse con características únicas que no estén fácilmente replicadas en otras plataformas, como la facilidad de uso combinada con opciones de personalización avanzada.

> Referencias:
> [10 webs para crear tu primer portafolio profesional [2024]](https://www.crehana.com/blog/transformacion-digital/5-webs-para-crear-tu-primer-portafolio-profesional/)
>
> [Muestra, descubre y contrata creativos :: Behance](https://www.behance.net/)
>
> [Dribbble - Discover the World's Top Designers & Creative Professionals](https://dribbble.com/)
>
> [LinkedIn](https://www.linkedin.com/)
>
> [Crear Página Web gratis | Creador de Páginas Web | Wix.com](https://es.wix.com/)

---

### Funcionalidades claves

#### 1. Gestión de Usuarios

- **Inicio de sesión**: Los usuarios pueden iniciar sesión en la plataforma con credenciales creadas mediante una pantalla de registro.
- **Perfil de usuario**: Cada usuario tiene un perfil que incluye información como nombre completo, correo electrónico, número de teléfono (opcional), país, redes sociales, imagen de perfil, y CV (subido a través de Cloudinary).
- **Idiomas**: Los usuarios pueden agregar y gestionar los idiomas que dominan, incluyendo el nombre del idioma y el nivel de fluidez.
- **Edición de perfil**: Los usuarios pueden editar su perfil, excepto el rol y el estado de la cuenta.
- **Redes sociales**: Los usuarios pueden añadir y gestionar los enlaces a sus perfiles de redes sociales.
- **Gestión de administradores**: Los administradores pueden gestionar los roles de los diversos usuarios y eliminar un portafolio o cuenta de usuario en caso de que se detecte mal uso de la plataforma.

#### 2. Gestión de portafolios

- **Creación de portafolios**: Los usuarios autenticados pueden crear un portafolio para mostrar su información profesional.
- **Personalización del portafolio**: Los usuarios pueden personalizar las secciones y subsecciones del portafolio, como el color de fondo, títulos de presentación, servicios ofrecidos, y el contenido de cada sección.
- **Slug único**: Cada portafolio tiene un slug único que permite a los usuarios acceder a su portafolio mediante una URL personalizada.
- **Visualización pública**: Los portafolios son visibles públicamente por cualquier visitante a través del slug o el id del portafolio.

#### 3. Secciones del portafolio

- **Sección principal (Home section)**: Incluye un título de presentación y un subtítulo con el cargo actual del usuario, acompañado de un fondo personalizable.
- **Sección de servicios (Services section)**: Los usuarios pueden listar y gestionar los servicios o especialidades que ofrecen.
- **Sección "sobre mí" (About section)**: Incluye un título de presentación, una frase sobre el tiempo de experiencia laboral y un contenido personalizado donde el usuario puede describirse.
- **Sección de resumen (Resume section)**:
  - **Sobre mí (About me)**: Contiene un resumen de la experiencia profesional del usuario y los años de experiencia.
  - **Experiencia profesional**: Los usuarios pueden añadir múltiples experiencias laborales, con detalles como fechas de inicio y fin, el nombre de la empresa y el cargo ocupado.
  - **Educación**: Los usuarios pueden agregar sus estudios, con información como fechas, nombre del curso, institución educativa y horas dedicadas al curso.
  - **Habilidades**: Los usuarios pueden listar sus habilidades profesionales.
  - **Secciones adicionales**: Los usuarios pueden agregar secciones personalizadas (e.g., proyectos, certificados, logros, voluntariado), cada una con su propio fondo y contenido.

#### 4. Gestión de Archivos

- **Subida de imágenes**: Los usuarios pueden subir su imagen de perfil a través de Cloudinary y mostrarla en el portafolio.
- **Subida de CV**: Los usuarios pueden subir su CV en formato PDF a través de Cloudinary para que esté disponible para descarga pública desde el portafolio.

#### 5. Funcionalidades de Administración

- **Control de acceso**: Los administradores son responsables de gestionar las cuentas de usuario.
- **Gestión de roles**: Los administradores tienen privilegios especiales para gestionar los usuarios, mientras que los usuarios estándar pueden gestionar solo su información.

#### 6. Visualización Pública de Portafolios

- **Portafolios de prueba**: La plataforma ofrece varios portafolios de prueba visibles para los visitantes, que muestran ejemplos de las funcionalidades que se pueden utilizar.
- **Acceso a portafolios**: Los visitantes pueden acceder a cualquier portafolio público mediante su slug o id.

#### 7. Seguridad y Privacidad

- **Autenticación**: Uso de JSON Web Tokens (JWT) o sesiones seguras para gestionar el inicio de sesión de los usuarios.
- **Autorización**: Control estricto de acceso para proteger las funcionalidades de edición de portafolio y administración.
- **Protección de datos**: Validación de los datos introducidos por los usuarios.

#### 8. Multilenguaje

- **Gestión de idiomas**: Los usuarios pueden desarrollar el portafolio en todos los idiomas que los usuarios deseen, otorgando las traducciones correspondientes.

---

### Tecnologías seleccionadas

| Categoría                          | Tecnología seleccionada |
| ---------------------------------- | ----------------------- |
| Base de datos                      | MongoDB                 |
| Backend                            | Express.js              |
| Frontend                           | Angular                 |
| Entorno de ejecución               | Node.js                 |
| Alojamiento de Imágenes y Archivos | Cloudinary              |

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

> Referencias:
> [MERN Stack: Qué es y qué ventajas ofrece | OpenWebinars](https://openwebinars.net/blog/mern-stack-que-es-y-que-ventajas-ofrece/)
>
> [What Is The MEAN Stack? Introduction & Examples | MongoDB](https://www.mongodb.com/resources/languages/mean-stack#:~:text=The%20MEAN%20stack%20is%20a,for%20use%20with%20cloud%20applications)
