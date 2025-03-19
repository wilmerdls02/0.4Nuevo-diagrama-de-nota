# 0.4Nuevo-diagrama-de-nota

#### Cuando se hace clic en el botón del formulario, el navegador enviará la entrada del usuario al servidor.

#### Cuando se envia el formulario se genera cinco solicitudes HTTP. La primera es el evento de envío de formulario.
#### Es una solicitud HTTP POST a la dirección del servidor new_note. con el código de estado HTTP 302. Se trata de una redirección de URL, con la que el servidor solicita al navegador que realice una nueva solicitud HTTP GET a la dirección definida en la Ubicación (Location) del encabezado - la dirección notes.

#### Entonces, el navegador vuelve a cargar la página de Notas. La recarga provoca tres solicitudes HTTP más: obtener la hoja de estilo (main.css), el código JavaScript (main.js) y los datos sin procesar de las notas (data.json).

#### La pestaña network también muestra los datos enviados con el formulario.

#### La etiqueta Form tiene atributos action y method, que definen que el envío del formulario se realiza como una solicitud HTTP POST a la dirección new_note. El código en el servidor responsable de la solicitud POST(este código está en el servidor, y no en el código JavaScript obtenido por el browse).

#### Los datos se envian como cuerpo de la solicitud Post.
#### El servidor puede acceder a los datos accediendo al campo req.body del objeto req de la solicitud.

#### El servidor crea un nuevo objeto de nota y lo agrega a un arreglo llamado notes.
