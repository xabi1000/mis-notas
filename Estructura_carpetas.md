/*******************  SASS  ******************/

Estructurar la carpeta SCSS.

1- lo primero es que tengo un archivo styles.SCSS que este va a ser el archivo donde importo todos los archivos .SCSS

2- la primera carpeta seria BASE
  en esta carpeta yo solo guardar el archivo de [_normalize.css] aparte de este archivo [_base.scss]
  [_base.scss] es donde yo establezco los estilos generales por ejemplo los del body, títulos, enlaces, imágenes, etc.
  en este archivo se usan solo etiquetas y son los que son comunes al proyecto supongamos por ejemplo que
  todos los títulos necesitan un color verde pues aquí pondría h1 h2 h3{color:red}, etc

3- la segunda carpeta seria COMPONENTS.
  en esta carpeta van todos los elementos que se repiten es decir botones, galerías, formularios, logos, elementos 
  que vamos a repetir en nuestra página como por ejemplo el icono del menú o un o un botón es algo que se repite a
  menudo en una página entonces yo aquí crearía mi archivo buttons por ejemplo [_botones.scss] una hoja para cada elemento 
  puede parecer complejo y que acabamos con unos proyectos muy grandes.

4- la tercera carpeta seria CONFIG.
  en esta carpeta van los archivos de configuración de del proyecto es decir variables fuentes cosas así
  colores por ejemplo un archivo [_colors.scss] un archivo [_fonts.scss] cosas así aquí el tema de la barra 
  baja es importante que lo pongáis cuando utilizáis compiladores de código que no sean automatizados 

5- la quinta carpeta seria HELPERS.
  en esta carpeta van todos archivos de ayuda, digamos que hemos creado una función que utilizamos en
  varios proyectos como por ejemplo el reseteo de las listas quitar el marcador de la lista quitarle el padding quitarle
  el margin esas cosas pues esa función iría en helpers entonces cada vez que la quisiéramos utilizar solo tendríamos que
  utilizar el include y llamar a esta función aquí.
  yo suelo meter funciones o archivos configuraciones ya de css que tengo escritas y que reutilizó.

6- la quinta sexta seria MIXINS.
  después tendríamos los mixins que esto es algo particular de esas los que sepáis SASS, sabéis que los mixins 
  son las funciones, yo aquí normalmente lo que hago es meter los break points por ejemplo [_breakPoints.scss],
  y aquí crearía mis funciones para el diseño responsive si tenemos reseteo en una función pues también los metería 
  aquí se funciones que nos sirvan para hacer el layout por ejemplo 
  con GRID o con FLEX-BOX también irían aquí todo el tema de funciones del proyecto irían en mixins.

7- la septima carpeta seria PAGES.
  en esta carpeta dar el estilo a las páginas que lo necesitan porque por ejemplo si tenemos una página
  de contacto como el formulario es un bloque es posible que esa página no tenga ningún estilo particular
  simplemente tendrá el estilo general de todas las páginas y además tendrá el bloque del formulario pero no tendrá
  ningún elemento particular esa página entonces en page lo que hago es meter los archivos que si necesitan una
  configuración especial si por ejemplo tenemos una página con con una galería de fotos y esa galería es un bloque pero
  además tengo un banner que sólo muestro en esa página pues ese estilo si podría dárselo aquí porque es un estilo propio
  de esa página en concreto entonces esta es la carpeta donde yo añado esas cosas.

/*******************  PUG  ******************/

Estructurar la carpeta VIEWS

1- la primera carpeta seria CONFIG.
  en esta carpeta van los archivos de configuración como las variables que sean propias del proyecto
  como por ejemplo una raíz del menú que es con lo que yo creo los menús empujo guardo todas las páginas 
  en un array y después lo recorro.

2- la seunda carpeta INCLUDES
  en esta carpeta el símil en sí sería el MIXINS los incluso de los mixinos perdón los blogs los include serían 
  los elementos html que vamos a repetir botones menús formularios lo que sea lo
  escribimos una sola vez y después lo incluimos en nuestro archivo de pug.

3- la tercera carpeta MIXINS.
  en esta carpeta van las funciones con las que creamos cosas si por ejemplo tenemos un mixin de html para crear 
  pues saber por ejemplo estamos recuperando usuarios de una base de datos y tenemos nuestra tarjetita de
  usuario pues en la carpeta mixing iría esa tarjetita de usuario para crear las cosas.

4- la cuarta carpeta PAGES
  en esta carpeta van las páginas del sitio lo que sería el home el gallery el contact about pues las típicas páginas 
  que tiene un proyecto.

5- la quinta carpeta TEMPLATE/S.
  en esta carpeta estaría template o templates dependiendo de si utilizáis una o varias templates lo que hace es guardar 
  el archivo común para todas las páginas entonces se escribe una sola vez y ahí ya tenéis toda la estructura común para 
  todo el proyecto en el caso de que queráis cambiar por ejemplo una clase que es general a todos los elementos a todas
  las páginas la cambiáis en template y al al procesarlo pues todos se cambia por lo cual a mí me parece muchísimo más
  cómodo luego el tema de los nombres pues eso ya es cosa de cada uno yo aquí suelo poner [template.pug] para el
  archivo base aquí cada una de las páginas los mixing pues cada uno de los mixing en un archivo y el nombre que
  tengan en incluso cada uno de esos bloques y el nombre que tengan sí aquí hemos creado el botón pues había
  un incluso que sería button punto o button sí pero no sería una carpeta eliminar sería el nuevo archivo button punto
  punto y así con todos los archivos

/*******************  JAVASCRIPT  ******************/

NOTA: La estructura de la carpeta de javascript es distinto en función del proyecto.

Estructurar la carpeta JS

lo primero es que tengo un archivo INDEX.JS que este va a ser el archivo donde importo todos los archivos .JS

1- la primera carpeta MODULES.
   normalmente en la carpeta MODULES se van guardando los archivos comunes a las páginas o sea el módulo 
   aquí se irían guardando cada uno de los archivos que necesitamos por ejemplo el archivo del menú,
   el archivo de la llamada del formulario, ...etc 
   cada función o cada archivo referente a un elemento en concreto iría dentro de módulos.

2- la primera carpeta HELPERS.
    en helpers se crean las funciones de ayuda si necesitamos una función común a todas las páginas por ejemplo
    no según un pop-up que salga cuando carga la página pues se crea aquí la función y lo único que se hace es
    llamarla en él lo que sería el [index.js] para que cuando el archivo haya cargado llamaríamos a nuestra función.
    