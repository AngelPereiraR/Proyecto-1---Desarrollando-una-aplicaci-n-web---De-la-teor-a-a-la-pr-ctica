# Proyecto 1: Desarrollando una aplicación web: De la teoría a la práctica

## Informe técnico

### Análisis de modelos de ejecución cliente-servidor

#### Definición

La **arquitectura cliente-servidor** es un modelo de diseño donde participan dos elementos:

- Cliente: Utiliza servicios.
- Servidor: Proporciona servicios.

Entre ambos debe haber una comunicación eficiente en red, habitualmente utilizando Internet.

En forma de resumen, todas las aplicaciones web son aplicaciones que utilizan la arquitectura cliente-servidor. El cliente es el navegador y el servidor sería la máquina donde se instalan las aplicaciones, las bases de datos y otros recursos que consumiría el cliente.

Actualmente se suele llamar con el término **backend** a la parte de las aplicaciones que funcionan como el servidor y se suele llamar con el término **frontend** a las aplicaciones que se ejecutan en el cliente.

#### Ejemplos de aplicaciones que utilizan el modelo cliente-servidor

El ejemplo más común de una aplicación cliente-servidor es un **servidor web**, en el cual el cliente envía una petición al servidor web para abrir una página web en cuestión, el servidor devuelve los datos y la página web se muestra en el navegador del cliente.

Otro ejemplo que también utiliza el principio cliente-servidor es un **servidor de correo electrónico**. Cuando un cliente se comunica con el servidor, el cliente recupera los correos electrónicos que están guardados en el servidor. En este caso, el servidor pone los correos electrónicos a disposición del cliente.

Por último, otra aplicación es la **transferencia de datos** entre un cliente y un servidor web, que permite subir y bajar archivos.

#### Tipos de arquitectura cliente-servidor

##### Arquitectura de dos niveles (2-tier)

Es el modelo habitual, donde los clientes realizan solicitudes **directamente** al servidor, sin que intervengan otros intermediarios.

##### Arquitectura de tres niveles (3-tier)

Se introduce un intermediario entre el cliente y el servidor normalmente para separar la capa de lógica de negocio. Esto aporta ventajas a nivel de **mantenibilidad y escalabilidad**, bajo el coste de una mayor complejidad.

##### Arquitectura de n niveles (n-tier)

Se añaden capas adicionales cuantas quiera tener el desarrollador en su proyecto. Esto permite **aislar aún más la responsabilidad del software**, siendo más complejo por cada capa añadida.

#### Ventajas y desventajas de la arquitectura cliente-servidor

##### Ventajas

- Administración central: el servidor está en el centro de la red. Todos los usuarios o clientes lo utilizan. Los recursos importantes, como bases de datos, se encuentran en el servidor y son accesibles de forma centralizada.
- Derechos de acceso controlados globalmente: el almacenamiento central de recursos importantes permite una gestión segura y global de los derechos de acceso.
- Escalabilidad: se puede aumentar la capacidad de clientes y servidores por separado.
- Fácil mantenimiento: al estar distribuidas las funciones y responsabilidades entre varios ordenadores independientes, es posible reemplazar, reparar, actualizar, o incluso trasladar un servidor, mientras que sus clientes no se verán afectados por ese cambio.
- Existen tecnologías suficientemente desarrolladas que aseguran la seguridad en las transacciones, la amigabilidad de la interfaz, y la facilidad de empleo.
- Los demás clientes no tienen acceso a las IP's por lo que se dificulta el rastreo y/o hackeo de los usuarios.

##### Desventajas

- Caída del servidor: debido a la disposición centralizada y a la dependencia en un modelo cliente-servidor, la caída del servidor conlleva la caída de todo el sistema.
- Recursos de un servidor: si el servidor tiene muy pocos recursos, afecta a todos los clientes.
- Inversión de tiempo: además de los conocimientos técnicos correspondientes, por ejemplo, para proteger y configurar servidores, su uso requiere una considerable inversión de tiempo.
- El software y el hardware de un servidor son generalmente muy determinantes. Un hardware regular de un ordenador personal puede no poder servir a cierta cantidad de clientes.
- El cliente no dispone de los recursos que puedan existir en el servidor.
- Los clientes no podrán compartir información entre ellos.

#### Comparativa de la arquitectura cliente-servidor con otras arquitecturas

##### Comparación con el software "standalone"

Una de las arquitecturas más frecuentes y tradicionales siendo la arquitectura predominante hace unos años es el software **"standalone"**, en el cual toda la operativa de la aplicación se ejecutaban en un único sistema. Se decidió empezar a desarrollar utilizando la arquitectura cliente-servidor para separar las responsabilidades y poder trabajar en la nube.

##### Comparación con las redes de pares

Las **redes de pares**, también conocidas como redes **par-a-par** o **peer-to-peer**, son redes de ordenadores en las que todos o algunos aspectos funcionan sin clientes ni servidores fijos, sino una serie de nodos que se comparten entre sí, actuando simultáneamente como clientes y servidores respecto a los demás nodos de la red.

La diferencia entre ambas se encuentra en que el modelo cliente-servidor tiene bien establecidos los roles de cada uno mientras que en las redes de pares, todos los componentes de la red actúan con ambos roles simultáneamente.

##### Comparación con la arquitectura Cliente-Cola-Cliente

Mientras la arquitectura cliente-servidor necesita que uno de sus componentes actúe como servidor, la arquitectura **Cliente-Cola-Cliente** habilita a todos los nodos para que actúen como clientes simples, mientras que el servidor actúa como una cola en la que se van añadiendo las peticiones de los clientes. Las redes de pares se basaron originalmente en este concepto.

> Referencias:
> [Cliente-servidor - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Cliente-servidor)
>
> [Peer-to-peer - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Peer-to-peer)
>
> [¿Cómo funciona el modelo cliente-servidor? - IONOS](https://www.ionos.es/digitalguide/servidores/know-how/modelo-cliente-servidor/)
>
> [Arquitectura cliente servidor: qué es, tipos y ejemplos](https://www.arsys.es/blog/todo-sobre-la-arquitectura-cliente-servidor)

---

### Evaluación, ventajas y desventajas de las tecnologías seleccionadas

| Categoría                          | Tecnología seleccionada |
| ---------------------------------- | ----------------------- |
| Base de datos                      | MongoDB                 |
| Backend                            | Express.js              |
| Frontend                           | Angular                 |
| Entorno de ejecución               | Node.js                 |
| Alojamiento de Imágenes y Archivos | Cloudinary              |

#### 1. MongoDB

**MongoDB** es una base de datos NoSQL que almacena datos como documentos binarios JSON. Tiene una alta flexibilidad y escabilidad, siendo muy adecuada como opción para aplicaciones que almacenan mucha información. A su vez, es multiplataforma, lo que te permite que sea utilizado dando igual en qué dispositivo se encuentre.

#### 2. Express.js

**Express.js** es un framework flexible y ligero para el desarrollo backend de aplicaciones Node.js. Actúa como interceptor para permitir una interacción fluida entre el cliente y la base de datos. A su vez ofrece sólidas capacidades de enrutado y un gestor de errores predeterminado.

#### 3. Angular

**Angular** es un framework de JavaScript diseñado para el desarrollo de interfaces frontend. Proporciona características como la vinculación de datos en ambas direcciones y la inyección de dependencias, lo que facilita la creación de vistas dinámicas y simplifica la construcción de interfaces de usuario complejas e interactivas.

#### 4. Node.js

**Node.js** es un entorno de ejecución multiplataforma y de código abierto para JavaScript. Permite ejecutar JavaScript en el lado del servidor y se caracteriza por una arquitectura basada en eventos y entradas/salidas no bloqueantes. Gracias a su enfoque asíncrono, es capaz de manejar varias solicitudes al mismo tiempo sin interrumpir la ejecución de otros procesos.

#### 5. Cloudinary

**Cloudinary** es una plataforma en la nube que permite gestionar, optimizar y entregar imágenes y videos. Ofrece herramientas para cargar, transformar y mejorar contenido multimedia, ayudando a mejorar el rendimiento de aplicaciones web y móviles mediante redes de distribución de contenido (CDN).

#### Ventajas y desventajas

##### Ventajas y Desventajas del Stack MEAN:

###### Ventajas:

- **Tecnologías basadas en JavaScript**: Todo el stack utiliza JavaScript (MongoDB, Express, Angular, Node.js), lo que facilita el desarrollo full-stack con un único lenguaje de programación.
- **Código reutilizable**: Permite compartir y reutilizar código tanto en el frontend como en el backend.
- **Escalabilidad**: MongoDB, como base de datos NoSQL, permite manejar grandes cantidades de datos no estructurados de manera eficiente.
- **Desarrollo ágil**: Herramientas como Node.js ofrecen una arquitectura basada en eventos, ideal para aplicaciones en tiempo real y escalables.
- **Comunidad y soporte**: Al ser un stack popular, cuenta con una gran comunidad, numerosos recursos y bibliotecas de terceros.

###### Desventajas:

- **Curva de aprendizaje**: A pesar de usar JavaScript en todo el stack, aprender y dominar cada tecnología (especialmente Angular y MongoDB) puede ser complicado.
- **No apto para todas las aplicaciones**: Aunque MongoDB es excelente para datos no estructurados, no es siempre la mejor opción para aplicaciones que requieren bases de datos relacionales.
- **Manejo de rendimiento**: La falta de reglas estrictas de esquema en MongoDB puede llevar a problemas de consistencia y rendimiento si no se gestiona adecuadamente.
- **Angular puede ser pesado**: En aplicaciones simples, Angular puede ser excesivo por su complejidad y tamaño.

##### Ventajas y Desventajas de Cloudinary:

###### Ventajas:

- **Optimización automática**: Cloudinary ajusta y optimiza automáticamente imágenes y videos para mejorar el rendimiento y la velocidad de carga en diferentes dispositivos y navegadores.
- **Transformación en tiempo real**: Permite manipular imágenes y videos dinámicamente, cambiando su tamaño, formato, calidad, entre otras características, sin necesidad de preprocesarlos.
- **Entrega rápida**: Utiliza redes de distribución de contenido (CDN) para ofrecer medios rápidamente en cualquier parte del mundo.
- **Compatibilidad con múltiples formatos**: Soporta una gran variedad de formatos de imagen y video, además de herramientas para la conversión automática.
- **Escalabilidad**: Maneja eficientemente grandes cantidades de contenido multimedia, ideal para aplicaciones de alto tráfico.

###### Desventajas:

- **Costos**: Aunque tiene planes gratuitos, el almacenamiento y uso intensivo de la plataforma pueden resultar costosos a medida que la aplicación escala.
- **Dependencia de terceros**: Confiar en una plataforma externa para la gestión de medios puede ser un riesgo en caso de caídas o problemas de conectividad.
- **Curva de aprendizaje**: Las múltiples opciones de transformación y gestión pueden ser abrumadoras para usuarios nuevos.
- **Limitaciones en el plan gratuito**: El plan gratuito tiene limitaciones en cuanto a almacenamiento, transformaciones y ancho de banda, lo que podría ser un problema para proyectos en crecimiento.

> Referencias:
> [MERN Stack: Qué es y qué ventajas ofrece | OpenWebinars](https://openwebinars.net/blog/mern-stack-que-es-y-que-ventajas-ofrece/)
>
> [Explicación de MEAN Stack: Componentes y ventajas](https://kinsta.com/es/blog/mean-stack/)
>
> [Mean Stack Vs Mern Stack: ¿Qué pila tecnológica elegir en 2023?](https://richestsoft.com/es/blog/mean-stack-vs-mern-stack/)

---

### Compatibilidad en navegadores, posibles problemas y soluciones respecto a las tecnologías seleccionadas

#### Compatibilidad y Problemas del Stack MEAN:

##### Compatibilidad:

- Angular: Funciona bien en navegadores modernos, pero puede fallar en versiones antiguas.

##### Problemas y Soluciones:

- **Navegadores antiguos**: Angular puede no funcionar. Solución: Usar polyfills.
- **Rendimiento en móviles**: Angular puede ser pesado. Solución: Optimización con lazy loading y AOT.
- **Rendering en tiempo real**: Carga en navegadores. Solución: Diseño eficiente y optimización de backend.

#### Compatibilidad y Problemas de Cloudinary:

##### Compatibilidad:

- Compatible con todos los navegadores modernos y adapta formatos automáticamente.

##### Problemas y Soluciones:

- **Formatos no soportados**: WebP no en todos los navegadores. Solución: Usar formatos de respaldo.
- **Carga lenta**: Recursos grandes pueden ser lentos. Solución: Optimización automática de calidad.
- **Conexiones lentas**: Videos pesados afectan. Solución: Lazy loading y streaming adaptativo.
- **Caché en CDN**: Cambios no inmediatos. Solución: Usar versioning o forzar actualización.

> Referencias:
> [LAMP vs MEAN: ¿Qué Stack Es el Adecuado para Ti? - Kinsta®](https://kinsta.com/es/blog/lamp-vs-mean/)
>
> [Version compatibility - Angular](https://angular.dev/reference/versions#browser-support)
>
> [6 consejos para mejorar el rendimineto de aplicaciones en Angular](https://itequia.com/es/6-consejos-para-mejorar-el-rendimiento-de-aplicaciones-en-angular/)
>
> [Image Management Best Practices](https://cloudinary.com/blog/4_image_management_best_practices)
>
> [WebP Format: Technology, Pros & Cons, and Alternatives](https://cloudinary.com/guides/front-end-development/webp-format-technology-pros-cons-and-alternatives)

---

### Análisis de los mecanismos de integración de los lenguajes de marcas con los lenguajes de programación de clientes web.

La **integración** entre los **lenguajes de marcas** (como HTML) y los **lenguajes de programación** del lado del cliente (como JavaScript) es fundamental para **crear páginas web dinámicas e interactivas**.

La integración se produce principalmente a través del **DOM**. El DOM es una representación de la página web como un **árbol de objetos**. JavaScript puede acceder y modificar estos objetos, lo que permite:

- **Manipular el contenido**: Agregar, eliminar o modificar texto, imágenes y otros elementos.
- **Cambiar el estilo**: Aplicar o eliminar clases CSS para cambiar la apariencia de los elementos.
- **Responder a eventos**: Detectar acciones del usuario, como clics, desplazamientos y cambios de tamaño de la ventana, y ejecutar código en respuesta.
- **Crear animaciones**: Utilizar el DOM y el temporizador de JavaScript para crear efectos visuales.
- **Realizar solicitudes al servidor**: Utilizar tecnologías como Fetch API o XMLHttpRequest para comunicarse con el servidor y obtener datos dinámicos.

> Referencias:
> [Lenguaje de marcado - Wikipedia, la enciclopedia libre](https://es.wikipedia.org/wiki/Lenguaje_de_marcado)
>
> [JavaScript: páginas web dinámicas con integración de marcado JavaScript](https://fastercapital.com/es/contenido/JavaScript--paginas-web-dinamicas-con-integracion-de-marcado-JavaScript.html#:~:text=La%20integraci%C3%B3n%20de%20marcado%20de%20JavaScript%20es%20un%20aspecto%20importante,funcionalidad%20y%20la%20experiencia%20del)
>
> [Introducción - Referencia de la API Web | MDN](https://developer.mozilla.org/es/docs/Web/API/Document_Object_Model/Introduction)

---

### Evaluación de herramientas de programación para clientes web, funciones y ventajas

#### Frameworks y Bibliotecas de JavaScript

##### React

- Funciones:
  - Biblioteca para construir interfaces de usuario mediante componentes reutilizables.
  - Utiliza un Virtual DOM para optimizar el rendimiento.
- Ventajas:
  - Componentización: Permite crear componentes encapsulados que manejan su propio estado.
  - Ecosistema rico: Amplia comunidad y una variedad de bibliotecas adicionales como Redux para gestión de estado.
  - Desarrollo reactivo: Ideal para aplicaciones de una sola página (SPA).

##### Angular

- Funciones:
  - Framework completo para desarrollar aplicaciones web de una sola página con TypeScript.
  - Incluye herramientas integradas para enrutamiento, gestión de formularios, y comunicación HTTP.
- Ventajas:
  - Arquitectura robusta: Ofrece un enfoque estructurado con inyección de dependencias y modularidad.
  - Actualizaciones automáticas: Usa el data binding bidireccional para sincronizar el modelo y la vista automáticamente.
  - Herramientas integradas: Menor necesidad de bibliotecas externas debido a su funcionalidad completa.

##### Vue.js

- Funciones:
  - Framework progresivo para construir interfaces de usuario que combina la simplicidad de HTML con la flexibilidad de JavaScript.
- Ventajas:
  - Curva de aprendizaje suave: Fácil de aprender y adaptar para desarrolladores nuevos.
  - Flexibilidad: Puede ser utilizado para proyectos pequeños y escalar a aplicaciones más complejas.
  - Documentación clara: Excelente documentación que facilita la adopción.

#### Preprocesadores CSS

##### Sass (Syntactically Awesome Style Sheets)

- Funciones:
  - Preprocesador CSS que permite el uso de variables, anidación, mixins y funciones.
- Ventajas:
  - Mantenibilidad: Facilita la organización del CSS y el manejo de estilos complejos.
  - Reutilización: Las variables y mixins permiten reutilizar estilos de manera eficiente.

##### LESS

- Funciones:
  - Similar a Sass, permite el uso de variables, anidación y funciones en CSS.
- Ventajas:
  - Simplicidad: Fácil de aprender y usar, con sintaxis más cercana a CSS estándar.

#### Herramientas de Construcción y Bundling

##### Webpack

- Funciones:
  - Herramienta de empaquetado que permite gestionar y agrupar recursos (JavaScript, CSS, imágenes).
- Ventajas:
  - Optimización: Permite la carga diferida (lazy loading) y la optimización de recursos para mejorar el rendimiento.
  - Configurabilidad: Altamente configurable, lo que permite adaptarse a diferentes flujos de trabajo.

##### Parcel

- Funciones:
  - Empaquetador web que requiere poca configuración.
- Ventajas:
  - Facilidad de uso: Configuración cero y rápida configuración inicial.
  - Rendimiento: Incluye optimizaciones automáticas sin necesidad de configuraciones complejas.

#### Gestores de Estado

##### Redux

- Funciones:
  - Biblioteca para gestionar el estado global de aplicaciones JavaScript.
- Ventajas:
  - Predecibilidad: Estado global centralizado que facilita la depuración.
  - Middleware: Soporta middleware para gestionar acciones asíncronas.

##### MobX

- Funciones:
  - Biblioteca para gestionar el estado que utiliza la programación reactiva.
- Ventajas:
  - Simplicidad: Más fácil de usar y menos boilerplate que Redux.
  - Reactividad automática: Actualizaciones automáticas de componentes sin necesidad de configuraciones adicionales.

#### Herramientas de Pruebas

##### Jest

- Funciones:
  - Framework de pruebas para JavaScript que permite pruebas unitarias y de integración.
- Ventajas:
  - Sencillez: Fácil de configurar y usar, con soporte para pruebas asíncronas.
  - Instantáneas: Permite pruebas de instantáneas para comparar la salida de componentes.

##### Cypress

- Funciones:
  - Herramienta para pruebas end-to-end que permite pruebas de interfaz de usuario en tiempo real.
- Ventajas:
  - Interactividad: Permite la depuración visual con una interfaz de usuario fácil de usar.
  - Velocidad: Ofrece pruebas rápidas con un enfoque en la experiencia del desarrollador.

#### Herramientas de Desarrollo y Debugging

##### Browser Developer Tools

- Funciones:
  - Herramientas integradas en navegadores (Chrome DevTools, Firefox Developer Edition) para inspeccionar y depurar código.
- Ventajas:
  - Interactividad: Permiten modificar el HTML y CSS en tiempo real y observar cambios inmediatamente.
  - Análisis de rendimiento: Ofrecen herramientas para analizar el rendimiento y optimizar el tiempo de carga.

##### Postman

- Funciones:
  - Herramienta para probar APIs que permite enviar solicitudes HTTP y analizar respuestas.
- Ventajas:
  - Facilidad de uso: Interfaz intuitiva que facilita la prueba de diferentes métodos HTTP.
  - Documentación de APIs: Permite documentar y compartir colecciones de pruebas.

> Referencias:
> [Frameworks JavaScript y librerías populares - IONOS España](https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/frameworks-javascript-y-librerias-populares/)
>
> [Preprocesador CSS - Glosario de MDN Web Docs: Definiciones de términos relacionados con la Web | MDN](https://developer.mozilla.org/es/docs/Glossary/CSS_preprocessor)
>
> [Comparando Bundlers de JavaScript: Rollup vs Webpack vs Parcel - Kinsta®](https://kinsta.com/es/blog/rollup-vs-webpack-vs-parcel/)
>
> [Las mejores 10 opciones para manejar nuestros estados en el Frontend - OpenExpo Europe 2024](https://openexpoeurope.com/es/las-mejores-10-opciones-para-manejar-nuestros-estados-en-el-frontend/)
>
> [11 mejores herramientas y marcos de pruebas unitarias de JavaScript | Geekflare](https://geekflare.com/es/javascript-unit-testing/)
>
> [Herramientas de Testing y Debugging para Desarrolladores](https://bigcode.es/herramientas-de-testing-y-debugging-para-desarrolladores/)

---

### Análisis de mercado detallando la competencia y como se diferencia la propuesta y su valor nuevo que aporta

#### Competencia Existente

A continuación, se presentan algunas de las principales plataformas de portafolios en línea y sus características clave:

##### Behance

- **Descripción**: Plataforma de Adobe enfocada en creativos (diseñadores, fotógrafos, ilustradores).
- **Características**:
  - Fuerte enfoque en el diseño visual.
  - Comunidad activa donde los usuarios pueden seguirse y comentar proyectos.
  - Integración con otras herramientas de Adobe.
- **Desventajas**: Limitaciones en la personalización de secciones y menos opciones para usuarios no creativos.

##### Dribbble

- **Descripción**: Red social para diseñadores y creativos que permite mostrar trabajos en formato de "shots".
- **Características**:
  - Focalización en el diseño gráfico y la UI/UX.
  - Posibilidad de recibir comentarios y "likes".
- **Desventajas**: Se centra en creativos, lo que puede excluir a otros profesionales que no se ajustan a este perfil.

##### LinkedIn

- **Descripción**: Red social profesional que permite a los usuarios crear un perfil profesional completo.
- **Características**:
  - Amplia visibilidad profesional y oportunidades de networking.
  - Posibilidad de mostrar experiencias laborales y educación.
- **Desventajas**: No es específicamente una plataforma de portafolios, por lo que carece de opciones de personalización para mostrar trabajos de manera visual.

##### WordPress/Wix

- **Descripción**: Plataformas de creación de sitios web que ofrecen plantillas para portafolios.
- **Características**:
  - Flexibilidad total en el diseño y personalización.
  - Posibilidad de crear sitios web completos, incluyendo portafolios.
- **Desventajas**: Requiere más tiempo y habilidades técnicas para crear un sitio funcional y estéticamente agradable.

#### Diferenciación y Valor Añadido de la Propuesta

El gestor de portafolios que se propone se diferencia de la competencia en varios aspectos clave:

##### Enfoque en Personalización y Usabilidad

- **Personalización avanzada**: Permite a los usuarios modificar múltiples secciones y subsecciones del portafolio, incluyendo títulos, descripciones, colores de fondo y más, superando las limitaciones de plataformas como Behance y Dribbble.
- **Simplicidad de uso**: La plataforma está diseñada para ser intuitiva, permitiendo a los usuarios crear y gestionar su portafolio en pocos pasos, sin la necesidad de habilidades técnicas avanzadas.

##### Acceso Abierto y Registro de Usuarios

- **Registro fácil**: A diferencia de plataformas que requieren invitaciones o limitan el acceso, esta propuesta permitirá el registro abierto para cualquier usuario, facilitando el acceso y la creación de portafolios sin restricciones administrativas.

##### Secciones Diversificadas

- **Múltiples tipos de secciones**: La posibilidad de añadir no solo experiencias laborales y educativas, sino también habilidades, proyectos, certificaciones y secciones personalizadas ofrece a los usuarios una forma integral de presentar su trayectoria profesional.

##### Integración de Archivos Multimedia

- **Subida de CV y multimedia**: Los usuarios pueden subir su CV y otros documentos a través de Cloudinary, lo que proporciona una gestión centralizada de los recursos visuales y documentos importantes, simplificando el proceso para los usuarios.

##### Adaptabilidad a Diversos Sectores

- **Atractivo multisectorial**: Mientras que plataformas como Behance y Dribbble están dirigidas a creativos, este gestor de portafolios se adapta a una gama más amplia de profesionales, incluidos técnicos, consultores y estudiantes.

##### Visibilidad Pública y Facilidad de Acceso

- **Portafolios públicos**: Los portafolios son accesibles públicamente a través de URL únicas, lo que facilita la visibilidad para empleadores y clientes potenciales, eliminando barreras de acceso.

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
