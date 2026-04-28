# Documentación del Proyecto: El Contrato Social

Este documento explica de manera detallada la organización del proyecto web y el funcionamiento paso a paso del formato de registro interactivo diseñado como una "solicitud formal".

---

## 1. Estructura de Carpetas

Para mantener un proyecto ordenado y profesional, el código está organizado de la siguiente manera:

*   **Carpeta `img/`:** Contiene todas las imágenes de la página (como `logo.png`, `inicio.png`, y fotografías). Esto mantiene limpio el entorno de trabajo y facilita ubicar los gráficos.
*   **Carpeta `paginas/`:** Contiene todas las páginas secundarias (`origen.html`, `Funcion.html`, `Enfoque.html`, `Actualidad.html` y el formulario `cuestionario.html`). Separar las vistas de la portada hace la navegación más estructurada.
*   **Archivo `index.html`:** Se encuentra en la raíz principal del proyecto. Es la página principal y punto de partida o "home" del sitio web.

**Sobre las rutas:** Todos los enlaces a imágenes en los archivos HTML utilizan rutas relativas (como `../img/` o `paginas/`). Esto garantiza que los archivos siempre puedan encontrarse sin importar si el proyecto se mueve a otra computadora o se sube a internet.

---

## 2. El Formulario de Registro (`cuestionario.html`)

Se adaptó el archivo para funcionar y verse como un formato altamente institucional y formal (similar a un contrato, una solicitud académica o de empleo). Aquí se detalla exactamente cómo funciona la estructura visual y técnica de este documento.

### A) Diseño Visual y Formato (CSS y Estructura)

Para lograr el aspecto de un "formato físico de registro" impreso, se usaron las siguientes técnicas:

1.  **Tipografía Clásica:** Se cambió el tipo de texto. Los encabezados e instrucciones utilizan fuentes con "patines" como **Times New Roman** o **serif**, las cuales proyectan una imagen legal o literaria. Para el contenido donde el usuario interactúa, se cambió a **Arial / sans-serif** por su máxima limpieza y legibilidad.
2.  **El Contenedor (Divisor "Caja"):** En vez de escribir sobre el fondo predeterminado, el formulario fue colocado dentro de un contenedor en HTML que llamamos `<div>`. A este contenedor se le dieron atributos especiales usando **CSS en línea** (`style="..."`):
    *   `background-color: #ffffff;`: Un fondo blanco sólido, idéntico a una hoja de papel.
    *   `border: 2px solid #000000;`: Un borde grueso en color negro que enmarca toda la solicitud.
    *   `padding: 30px;`: Margen interno para que el texto no toque la "pared" negra de la caja, dando un efecto respirable y elegante.
    *   `box-shadow:`: Un sombreado que da la ilusión de que la "hoja de papel" está flotando sobre el fondo de la pantalla.
3.  **Encabezados Formales (`<h1>`, `<h2>`):** Sustituimos las fuentes de colores por un diseño austero de blanco y negro para potenciar el carácter de "documento oficial", e insertamos las líneas divisorias horizontales (`<hr>`).

### B) Recopilación de Datos (Etiquetas Inputs paso a paso)

Dentro del contenedor oficial establecimos la zona de trabajo usando la etiqueta HTML `<form>`. Todo lo que se escriba aquí estará preparado para ser "enviado". Cada campo utiliza un tipo específico de `input` para controlar qué y cómo introduce datos el usuario:

*   **Nombre Completo:**
    *   `Etiqueta utilizada:` `<input type="text">`
    *   `Descripción:` Se le aplica el texto guía transparente (*placeholder*) "Apellido Paterno / Apellido Materno / Nombre(s)" para imponer formalidad. La etiqueta "text" permite texto libre de un renglón.
    *   `Estético:` Se le dio un marco negro sólido de 1 píxel al cuadro (`border: 1px solid #000`) para simular las cajas vacías de un formato a mano.

*   **Correo Electrónico:**
    *   `Etiqueta utilizada:` `<input type="email">`
    *   `Descripción:` Es especial. Cuando el usuario escriba algo y le dé "Enviar", el mismo navegador web no lo dejará continuar a menos que valide que lo escrito tiene estructura de correo válida (que tenga por lo menos el símbolo `@`).

*   **Número de Teléfono:**
    *   `Etiqueta utilizada:` `<input type="tel">`
    *   `Descripción:` Configurado para telefonía. En computadoras luce normal, pero si este proyecto se abre desde un teléfono celular, forzará a que salga el teclado numérico en pantalla asumiendo que vas a escribir un teléfono.

*   **Edad:**
    *   `Etiqueta utilizada:` `<input type="number">`
    *   `Descripción:` El navegador lo convierte en un control especial que solo acepta números, agregando también unas pequeñas flechas (spinners) para que el usuario pueda sumar o restar números mediante clics sin tener que teclearlos.

*   **Fecha de Nacimiento:**
    *   `Etiqueta utilizada:` `<input type="date">`
    *   `Descripción:` Uno de los elementos más interactivos. Automáticamente le da a la página la capacidad de mostrar un "calendario flotante" desplegable para que la persona oprima los números desde un calendario visual sin error de formato.

*   **Comentarios y Opiniones:**
    *   `Etiqueta utilizada:` `<textarea>`
    *   `Descripción:` A diferencia del `text`, un `textarea` expone un rectángulo bastante espacioso (con la propiedad de renglones *rows* y columnas *cols*) diseñado para aceptar múltiples párrafos sin cortarse. 

### C) Botones Interfaz (Procesamiento)

*   **Enviar Solicitud:** `<input type="submit">` es el botón clave, estilizado en **negro intenso y con letras blancas**. Se encarga de correr las validaciones (revisar que escribieran el nombre y de que el correo contenga el "@") e intenta mandar los datos procesados.
*   **Limpiar Formato:** `<input type="reset">` es el botón secundario en color gris. Permite vaciar y blanquear absolutamente todos los cuadros de entrada devolviendo el documento a su estado inicial.

## 3. Conclusión

Este proyecto no sólo contiene y distribuye información enlazada sobre el Contrato Social a través de `index.html` y la carpeta `paginas/`, sino que aporta interacción de datos, estilos tipo "Contrato Oficial" en los formularios, y uso de múltiples controles interactivos mediante HTML avanzado y enrutamiento relativo.
