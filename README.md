# Guía de vtex
<h3>
  Mini guía para manejar Vtex, algunos de sus componentes y configuraciones.
</h3>

<hr>

<h2>Indice:</h2>
<ul>
  <li><a href="#templates">Templates</a></li>
  <li><a href="#subtemplates">Subtemplates</a></li>
  <li>
    <a href="#placeholders">Placeholders</a>
    <ol>
      <li><a href="#asignarplaceholder">Asignar un placeholder</a></li>
      <li><a href="#configurarplaceholder">Configurar un placeholder</a></li>
      <li><a href="#typesplaceholder">Tipos de placeholder</a></li>
    </ol>
  </li>
  <li>
    <a href="#layouts">Layouts</a>
    <ol>
      <li><a href="#entornos">Entorno público y privado(LID:)</a></li>
    </ol>
  </li>
</ul>

<hr />

<h4>Ingresar al CMS:</h4>
<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/go-to-cms.gif" />

<hr>

<h2 id="templates">Templates:</h2>

<h4>Crear/editar un template:</h4>

<p>Vamos a: </p>
<ul>
  <li>Para crear: <code>CMS > HTML Templates > new template</b></code></li>
  <li>Si sólo queremos editar: <code>CMS > HTML Templates > {nombre del template a editar}</b></code></li>
  <li>le asignamos/cambiamos un nombre en <b>Template Name:</b></li>
  <li>dentro del box <b>Template XHTML:</b> colocamos/cambiamos el contenido HTML</li>
  <li>Guardamos el contenido con <b>Save template</b></li>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-template.gif" />

<hr>

<h2 id="subtemplates">Subtemplates:</h2>

<h4>Crear/editar un subtemplate:</h4>

<p>Un subtemplate es un complemento de vtex, ante la necesidad de usar una especie de include, una parte de codigo q podemos reutilizar poniéndosela dentro de uno/varios templates como para tener que cambiarlo solo una vez y este cambio se vea replicado
  en todos los templates, sin necesidad de hacerlo uno por uno. Para esto vamos a: </p>
<ul>
  <li>Para crear: <code>CMS > HTML Templates > new template</b></code></li>
  <li>Si sólo queremos editar: <code>CMS > HTML Templates > Sub Templates > new sub template {o bien usamos/cambiamos unos ya existente}</b></code></li>
  <li>le asignamos/cambiamos un nombre en <b>Template Name:</b>, este será nuestro ID de sub template</li>
  <li>dentro del box <b>Template XHTML:</b> colocamos/cambiamos el contenido HTML</li>
  <li>Guardamos el contenido con <b>Save template</b></li>

  <li>Para asignarlo vamos a un <b>Template</b> que queramos, y usamos el complemento de vtex (como tag html <code>< /></code>) junto con el ID/nombre de subtemplate que le habíamos asignado previamente <b>vtex:template id="{tu_ID}"</b>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-subtemplate.gif" />

<hr>

<h2 id="placeholders">Placeholders:</h2>

<p>Un placeholder, es un complemento de vtex, donde podemos colocar contenido HTML, es parecido al subtemplate (su sintaxis), salvo que tiene otras funcionalidades, que aparecerán una vez colocado en el template (el complemento mencionado), y asignado el
  template en un layout, en la configuración de este último.

  <h4 id="asignarplaceholder">Asignar un placeholder a un template:</h4>

  <p>Para asignar un placeholder: </p>
  <ul>
    <li><code>CMS > HTML Templates > {template al que se le agrega el placeholder}</b></code></li>
    <li>Se agrega el complemento en el HTML (como tag html <code>< /></code>): <code>vtex:contentPlaceHolder id="ID_del_placeholder"</code></li>
    <li>Guardamos el contenido con <b>Save template</b></li>
  </ul>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-subtemplate.gif" />
  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/add-placeholder.png" />

  <h4 id="configurarplaceholder">Configurar un placeholder:</h4>

  <p>Podemos darle el formato al placeholder asignado</p>
  <ul>
    <li>Vamos al layout que hayamos modificado o bien le aplicamos el template al layout que queremos, y vamos a la pestaña <b>Settings</b></li>
    <li>Encontramos el placeholder con el <code>ID</code> que le hayamos asignado, añadimos y seleccionamos el tipo de placeholder que será, y guardamos el layout</li>
    <li>volvemos a ingresar nuevamente al layout, para que impacte la asignación, y ya podemos editar sobre el mismo</li>
  </ul>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-subtemplate.gif" />

  <h4 id="typesplaceholder">Tipos de placeholder</h4>
  <p>
    Podemos setear el placeholder para que funcione de determinada manera. Como es el caso de los siguientes (los más utilizados):
  </p>
  <ul>
    <li>
      HTML - (Permite agregar codigo HTML)
    </li>
    <li>
      Colección (permite agregar una lista de productos por ID, por ejemplo: "Todos los productos - ID es: 140")
    </li>
    <li>
      Banner (Permite agregar imágenes/banners/banners Flash, con un tamaño especifico)
    </li>
  </ul>
</p>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/types-placeholder.png" />

<hr>

<h2 id="layouts">Layouts</h2>

<h4>Crear/editar un Layout:</h4>

<p>El layout, es donde se va a asignar el template y poder visualizarlo con su respectiva URL:</p>
<ul>
  <li><code>CMS > Sites and channels > fravega (o valkiriaqa) > / > "carpeta en donde queremos crear/cambiar el layout" </b></code></li>
  <li>Le asignamos un nombre en <b>Layout name:</b></li>
  <li>Dentro del select <b>Template:</b> seleccionamos/cambiamos el template para asignarselo</li>
  <li>Podemos tambien si fuera necesario asignarle clases al body en <b>Body Class:</b> (por defecto siempre ponemos <code>title_seo</code>, y cualquier otra si fuera necesario)</li>
</ul>

<h4 id="entornos">
  Entornos de layout
</h4>

<p>Los layout pueden mostrarse de manera pública, o de forma privada solo pegando el código LID</p>

<ul>
  <li><b>IMPORTANTE!</b> si el layout queda con el checkbox tildado: <code>Default page:</code>(además de <b>Active:</b> que viene tildado por defecto) queda pública la URL! </li>
  <li>Si quisieramos ver el contenido de un layout que NO és público(sin la casilla Default quede tildada), lo podemos ver por el <code>lid</code> que se encuentra arriba del <b>Layout name:</b> (en el caso del video seria: <code>http://www.fravega.com/<b>?lid=724ebe5e-a94a-47b2-8fd6-bf52d259535b</b></code>)
    <li>Guardamos el contenido con <b>Save Layout</b></li>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/show-lid.png" />
