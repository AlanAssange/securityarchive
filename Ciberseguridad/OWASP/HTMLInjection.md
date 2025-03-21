# HTML Injection

La inyección de HTML es una vulnerabilidad que ocurre cuando la entrada del usuario no filtrada se muestra en la página. Si un sitio web no sanitiza la entrada del usuario (es decir, no filtra cualquier texto "malicioso" que un usuario ingresa en el sitio), y esa entrada se utiliza en la página, un atacante puede inyectar código HTML en un sitio web vulnerable.

La sanitización de la entrada es muy importante para mantener un sitio web seguro, ya que la información que un usuario ingresa en un sitio web a menudo se utiliza en otras funciones del frontend y backend.

Cuando un usuario tiene control sobre cómo se muestra su entrada, puede enviar código HTML (o JavaScript), y el navegador lo utilizará en la página, lo que permite al usuario controlar la apariencia y funcionalidad de la página.

Ejemplo:
Un input de nombre de usuario puede llevar a insertar un tag de link y que se visualice en la pagina.

Inserte su nombre de usuario:
y alli inserto el A HREF que luego sera visualizado en la pagina.
