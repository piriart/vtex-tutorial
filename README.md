# Guía de vtex
<h3>
  Mini guia para manejar Vtex, algunos de sus componentes y configuraciones.
</h3>

<hr>

<h4>Ingresar al CMS:</h4>
<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/go-to-cms.gif" />

<hr>

<h4>Crear un nuevo template:</h4>

<p>Vamos a: 
<ul>
  <li><code>CMS > HTML Templates > new template</b></code></p></li>
  <li>le asignamos un nombre en <b>Template Name:</b></li>
  <li>dentro del box <b>Template XHTML:</b> ponemos el contenido HTML</li>
  <li>Guardamos el contenido con <b>Save template</b></li>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-template.gif" />

<hr>

<h2>Layouts</h2>

<h4>Crear/editar un nuevo Layout:</h4>

<p>El layout, es donde se va a asignar el template para que sea publico(o bien privado), y poder visualizarlo con su respectiva URL(URL con LID si es privado).
Vamos a: 
<ul>
  <li><code>CMS > Sites and channels > fravega (o valkiriaqa) > / > "carpeta en donde queremos crear el nuevo layout" </b></code></p></li>
  <li>Le asignamos un nombre en <b>Layout name:</b></li>
  <li>Dentro del select <b>Template:</b> seleccionamos/cambiamos el template para asignarselo</li>
  <li>Podemos tambien si fuera necesario asignarle clases al body en <b>Body Class:</b> (por defecto siempre ponemos <code>title_seo</code>, y cualquier otra si fuera necesario)</li>
  <li><b>IMPORTANTE!</b> si el layout queda con el checkbox tildado: <code>Default page:</code>(además de <b>Active:</b> que viene tildado por defecto) queda pública la URL! </li>
  <li>Si quisieramos ver el contenido de un layout que NO és público(sin la casilla Default quede tildada), lo podemos ver por el <code>lid</code> que se encuentra arriba del <b>Layout name:</b> (en el caso del video seria: <code>http://www.fravega.com/<b>?lid=724ebe5e-a94a-47b2-8fd6-bf52d259535b</b></code>)
  <li>Guardamos el contenido con <b>Save Layout</b></li>
</ul>

<img src="https://github.com/fravega/vtex-tutorial/blob/master/images/create-new-layout.gif" />
