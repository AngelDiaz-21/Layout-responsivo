# Proyecto Apeperia

Archivos iniciales del proyecto para Apeperia del curso "Layouts Responsivos: Trabajando con layouts mobile", de Alura LATAM.

**Link para ver el diseño en figma**: [Ver página](https://www.figma.com/file/Cv9OIfwW20qbM2ywcSXOnK/Apeperia-Mobile-First-(inicial)?node-id=15%3A198)

## ¿Que se aprendió a lo largo del curso?
* Analizar y separar el layout recibido.
* Saber como funcionan las unidades relativas `REM` y `EM` así como el tipo de imágenes.
* Qué es y para que sirve mobile-first.
* Cómo funciona el initial-scale dentro del contenido Viewport.
* Como declarar y llamar a las variables CSS.
* Utilizar las unidades de viewport.
* Identificar la diferencia entre las unidades absolutas y relativas.
* Analizar las limitaciones físicas de los dispositivos.
* Cómo trabajar con las imágenes del layout.
* La importancia de escribir un código semántico.
* Crear estilos diferentes para diversos dispositivos con media queries.
* Adaptar la estructura y el contenido para diseños/layouts diferentes.

**Notas**
* Cuando se crean páginas para diferentes dispositivos, es importante utilizar unidades de medidas que se adapten automáticamente para múltiples tamaños y espacios. A veces es interesante utilizar unidades que sean relativas a otras situaciones, como es el caso de `REM` y `EM`.
  * `REM` es una unidad relativa a la propiedad `font-size` de la etiqueta, por lo tanto, si la etiqueta tiene 16px de `font-size` 1 `REM` equivale a 16px. `EM` es relativa a la propiedad `font-size` de la etiqueta madre, por lo tanto, si la etiqueta madre es un `font-size` de 16px, 1 `EM` equivale a 16px.
* ¿Cuándo utilizar SVG? 
  * Logotipos.
  * Íconos.
  * Ilustraciones más sencillas o imágenes simplificadas.
* El PNG suele usarse en imágenes con más detalles y colores.
* Para seguir un concepto de desarrollo, sea mobile-first o sea desktop-first se deben evaluar las necesidades del proyecto y analizar todos los puntos que influencian en el proyecto.
* Motivaciones de utilizar el desarrollo mobile-first:
  * Gran parte de los accesos y ventas son de dispositivos móviles.
  * El diseño es minimalista y simplificado.
  * Enfoque en el contenido.
* Motivaciones para utilizar el desarrollo desktop-first:
  * La interfaz tiene features más ricas.
  * Mayor capacidad de ejecución de las instrucciones.
  * El producto es optimizado para desktop (ejemplo: Google Docs).
* El meta viewport ayuda a reconocer que la página se esta visualizando en un sitio móvil y dentro del meta también se coloca el contenido que en este caso el tamaño es igual al tamaño del dispositivo que se este utilizando, también se coloca el parámetro que indica la escala inicial.
* Para declarar una variable se logra con el selector `:root{}`, escribiendo el `--nombre-de-la-variable: valor` y para llamar las variables según la sintaxis se realiza lo siguiente `var(--nombre-de-la-variable)`.
* Las unidades de viewport son unidades relativas, como por ejemplo, el porcentaje. Para que una imagen ocupe toda la anchura de la pantalla se debe de indicar como valor `100vw` en la propiedad `width`.
* Al momento de utilizar una imagen se pueden usar las propiedades `width` y `max-width`, donde en la propiedad `width` se podría indicar que tenga como valor una unidad relativa como sería viewport(`vw`) y porcentaje(`%`) esto para definir en pantallas menores. Y en cambio, en la propiedad `max-width` se puede utilizar una unidad absoluta como lo sería pixeles(`px`) para limitar las pantallas mayores, porque si solo se deja la unidad relativa a medida que crezca el ancho de pantalla también lo hará la imagen logrando que se deforme o se vea fea. Así que una vez que crezca la pantalla la imagen adoptará un ancho definido. Desde mi punto de vista es una buena idea, creo que se podría ahorrar líneas de códigos al momento de hacer el responsive design así como también dejar en `width` un valor con una unidad relativa y `max-width` un valor con una unidad absoluta.
* Para colocar una dirección se debe utilizar la etiqueta `<address></address>`, lo que ayudaría a mejorar la accesibilidad de la página.
* El número de teléfono y el correo se pueden colocar dentro de una etiqueta `<a></a>` y dentro del atributo `href` se podría hacer lo siguiente:
  * En el caso del teléfono: `href="tel:+551155712751"`.
  * En el caso del correo: `href="mailto:contacto@apeperia.com"`.
    El número de teléfono se coloca sin espacios, ya dentro de la etiqueta si. Y también se puede obervar que se coloca `tel:`, esto va a permitir que se abra una aplicación donde se puede usar el número de teléfono y lo mismo sucede con el email, solo que este caso `mailto:` abre una aplicación para enviar un correo.
* En la etiqueta `<video>` se puede usar el atributo `controls` que permite mostrar los controles del player (play, pause, volumen…).
* ¿Cuáles son las principales ventajas de escribir un código semántico?
  * Para que otras personas desarrolladoras puedan entender.
  * Para atender a los requisitos de accesibilidad. Debemos dejar nuestra página lo más inclusiva y para eso precisamos utilizar todas las etiquetas correctas para demarcar todo el contenido de la página web
  * Para herramientas de indexación. Hay muchos bots (herramientas automáticas) que verifican todo el código de nuestro proyecto, después hacen una validación para cambiar el posicionamiento de nuestra página en los resultados de motores de búsqueda (ejemplo: Google).