# Guía de vtex
<h3>
  Mini guía para manejar Vtex, algunos de sus componentes y configuraciones.
</h3>

<hr>

<h2>Indice:</h2>
<ul>
  <li><a href="#ingresaralcms">Ingresar al CMS</a></li>
  <li><a href="#templates">Templates</a></li>
  <li><a href="#subtemplates">Subtemplates</a></li>
  <li>
    <a href="#placeholders">Placeholders</a>
    <ul>
      <li><a href="#asignarplaceholder">Asignar un placeholder</a></li>
      <li><a href="#configurarplaceholder">Configurar un placeholder</a></li>
      <li>
        <a href="#typesplaceholder">Tipos de placeholder</a>
        <ul>
          <li><a href="#placeholder-html">Placeholder HTML</a></li>
          <li><a href="#placeholder-coleccion">Placeholder colección</a></li>
          <li><a href="#placeholder-banner">Placeholder banner</a></li>
        </ul>
      </li>
      </lu>
  </li>
  <li>
    <a href="#layouts">Layouts</a>
    <ul>
      <li><a href="#crearLayout">Crear un nuevo layout</a></li>
      <li><a href="#asignaruntemplatealayout">Asignar un template al layout</a></li>
      <li><a href="#crearCarpeta">Crear una nueva carpeta para un layout</a>
        <ul>
          <li><a href="#assignarcoleccionacarpeta">Asignar colección a una carpeta tipo de resultado de búsqueda</a></li>
        </ul>
      </li>
      <li><a href="#entornos">Entorno público y privado(LID:)</a></li>
    </ul>
  </li>
  </ul>

  <hr />

  <h4 id="ingresaralcms">Ingresar al CMS:</h4>
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

  <br>
  <br>

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

    <li>Para asignarlo vamos a un <b>Template</b> que queramos, y usamos el complemento de vtex (como tag html <code>< /></code>) junto con el ID/nombre de subtemplate que le habíamos asignado previamente <b>vtex:template id="{tu_ID}"</b></li>
  </ul>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-subtemplate.gif" />
  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/add-subtemplate.png" />

  <hr>

  <h2 id="placeholders">Placeholders:</h2>

  <p>Un placeholder, es un complemento de vtex, donde podemos colocar contenido HTML, es parecido al subtemplate (su sintaxis), salvo que tiene otras funcionalidades, que aparecerán una vez colocado en el template (el complemento mencionado), y asignado
    el template en un layout, en la configuración de este último.</p>

  <h4 id="asignarplaceholder">Asignar un placeholder a un template:</h4>

  <p>Para asignar un placeholder: </p>
  <ul>
    <li>Desde: <code>CMS > HTML Templates > {template al que se le agrega el placeholder}</b></code></li>
    <li>Se agrega el complemento en el HTML (como tag html <code>< /></code>): <code>vtex:contentPlaceHolder id="ID_del_placeholder"</code></li>
    <li>Guardamos el contenido con <b>Save template</b></li>
  </ul>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/add-placeholder.png" />

  <h4 id="configurarplaceholder">Configurar un placeholder:</h4>

  <p>Podemos darle el formato al placeholder asignado</p>
  <ul>
    <li>Vamos al layout que hayamos modificado o bien le aplicamos el template al layout que queremos, y vamos a la pestaña <b>Settings</b></li>
    <li>Encontramos el placeholder con el <code>ID</code> que le hayamos asignado, añadimos y seleccionamos el tipo de placeholder que será, y guardamos el layout</li>
    <li>volvemos a ingresar nuevamente al layout, para que impacte la asignación, y ya podemos editar sobre el mismo</li>
  </ul>

  <br>
  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-placeholder.gif" />

  <h4 id="typesplaceholder">Tipos de placeholder</h4>
  <p>
    Podemos setear el placeholder para que funcione de determinada manera, según el tipo que le asignemos, también a los placeholder se puede asignar con fecha de inicio y finalización, pudiendo así darle una fecha y horario predefinido. Los placeholders
    más utilizados son:
  </p>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/types-placeholder.png" />

  <br>

  <ul>
    <li id="placeholder-html">
      Placeholder HTML - (Permite agregar codigo HTML) <br><br>
      <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/placeholder-html.gif" />
      <br>
    </li>
    <li id="placeholder-coleccion">
      Placeholder Colección
      <ul>
        <li>Se asigna el Layout que queremos usar para la coleccion</li>
        <li>numero de filas y columnas(cantidad de productos que se van a mostrar)</li>
        <li>se asigna la lista por ID o nombre (por ejemplo: "productos Cyber ID es: 150")</li>
      </ul>
      <br>
      <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/placeholder-coleccion.gif" />
      <br>
    </li>
    <li id="placeholder-banner">
      Placeholder Banner (Permite agregar imágenes/banners/banners Flash, con un tamaño específico)
      <br><br>
      <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/placeholder-banner.gif" />
      <br>
    </li>
  </ul>

  <hr>

  <h2 id="layouts">Layouts</h2>

  <h4 id="crearLayout">Crear/editar un Layout:</h4>

  <p>
    El layout, es donde se va a asignar el template HTML y nos dara una URL (pública o privada).<br/> Desde los Layout podemos:
  </p>

  <ul>
    <li>Desde: <code>CMS > Sites and channels > fravega (o valkiriaqa) > / > "carpeta en donde queremos crear/cambiar layout" </b></code></li>
    <li>Dentro del select <b>Template:</b> seleccionamos/cambiamos el template para asignarselo</li>
    <li>Podemos tambien si fuera necesario asignarle clases al body en <b>Body Class:</b> (por defecto siempre ponemos <code>title_seo</code>, y cualquier otra si fuera necesario)</li>
  </ul>
  <br>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-layout.png" />

  <br>

  <h4 id="crearCarpeta">
    Creando una carpeta:
  </h4>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/new-folder.gif" />

  <br>

  <h4 id="asignaruntemplatealayout">
    Asignandole un template a un Layout:
  </h4>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-layout.gif" />

  <br>

  <h4 id="assignarcoleccionacarpeta">
    Asignar una colección a una carpeta
  </h4>
  <p>
    Es posible asignar una colección de productos a una carpeta para que levante como un resultado de búsqueda el layoout interno.
  </p>

  <br>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/add-collection-to-folder.png" />

  <h4 id="entornos">
    Entornos de layout:
  </h4>

  <p>Los layout pueden mostrarse de manera pública, o de forma privada solo pegando el código LID</p>

  <ul>
    <li><b>IMPORTANTE!</b> si el layout queda con el checkbox tildado: <code>Default page:</code>(además de <b>Active:</b> que viene tildado por defecto) queda pública la URL! </li>
    <li>Si quisieramos ver el contenido de un layout que NO és público(sin la casilla Default quede tildada), lo podemos ver por el <code>lid</code> que se encuentra arriba del <b>Layout name:</b> (en el caso del video seria: <code>http://www.fravega.com/<b>?lid=724ebe5e-a94a-47b2-8fd6-bf52d259535b</b></code>)
      <li>Guardamos el contenido con <b>Save Layout</b></li>
  </ul>
  <br>

  <img src="https://github.com/fravega/vtex-tutorial/blob/master/images/show-lid.png" />
