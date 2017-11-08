# Guía de vtex
<h3>
  Mini guia para manejar Vtex, algunos de sus componentes y configuraciones.
</h3>

<hr>

<h4>Ingresar al CMS:</h4>
<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/go-to-cms.gif" />

<hr>

<h2>Templates:</h2>

<h4>Crear/editar un template:</h4>

<p>Vamos a: </p>
<ul>
  <li>Para crear: <code>CMS > HTML Templates > new template</b></code></p></li>
  <li>Si sólo queremos editar: <code>CMS > HTML Templates > {nombre del template a editar}</b></code></p></li> 
  <li>le asignamos/cambiamos un nombre en <b>Template Name:</b></li>
  <li>dentro del box <b>Template XHTML:</b> colocamos/cambiamos el contenido HTML</li>
  <li>Guardamos el contenido con <b>Save template</b></li>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-template.gif" />

<hr>

<h2>Subtemplates:</h2>

<h4>Crear/editar un subtemplate:</h4>

<p>Un subtemplate es un complemento de vtex, ante la necesidad de usar una especie de include, una parte de codigo q podemos reutilizar poniendosela dentro de uno/varios templates como para tener que cambiarlo solo una vez y este cambio se vea replicado en todos los templates, sin necesidad de hacerlo uno por uno.
Para esto vamos a: </p>
<ul>
  <li>Para crear: <code>CMS > HTML Templates > new template</b></code></p></li>
  <li>Si sólo queremos editar: <code>CMS > HTML Templates > Sub Templates > new sub template {o bien usamos/cambiamos unos ya existente}</b></code></p></li> 
  <li>le asignamos/cambiamos un nombre en <b>Template Name:</b>, este será nuestro ID de sub template</li>
  <li>dentro del box <b>Template XHTML:</b> colocamos/cambiamos el contenido HTML</li>
  <li>Guardamos el contenido con <b>Save template</b></li>
  <li>Para asignarlo vamos a un <b>Template</b> que queramos, y usamos el complemento de vtex junto con el ID/nombre de subtemplate que le habiamos asignado previamente <b>vtex:template id="{tu_ID}"</b>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-subtemplate.gif" />

<hr>

<h2>Layouts</h2>

<h4>Crear/editar un Layout:</h4>

<p>El layout, es donde se va a asignar el template para que sea publico(o bien privado), y poder visualizarlo con su respectiva URL(URL con LID si es privado).
Vamos a:</p>
<ul>
  <li><code>CMS > Sites and channels > fravega (o valkiriaqa) > / > "carpeta en donde queremos crear/cambiar el layout" </b></code></p></li>
  <li>Le asignamos un nombre en <b>Layout name:</b></li>
  <li>Dentro del select <b>Template:</b> seleccionamos/cambiamos el template para asignarselo</li>
  <li>Podemos tambien si fuera necesario asignarle clases al body en <b>Body Class:</b> (por defecto siempre ponemos <code>title_seo</code>, y cualquier otra si fuera necesario)</li>
  <li><b>IMPORTANTE!</b> si el layout queda con el checkbox tildado: <code>Default page:</code>(además de <b>Active:</b> que viene tildado por defecto) queda pública la URL! </li>
  <li>Si quisieramos ver el contenido de un layout que NO és público(sin la casilla Default quede tildada), lo podemos ver por el <code>lid</code> que se encuentra arriba del <b>Layout name:</b> (en el caso del video seria: <code>http://www.fravega.com/<b>?lid=724ebe5e-a94a-47b2-8fd6-bf52d259535b</b></code>)
  <li>Guardamos el contenido con <b>Save Layout</b></li>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-layout.gif" />
