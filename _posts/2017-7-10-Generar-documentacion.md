---
published: true
layout: post
category: angular
tags:
  - angular
---
La generación de documentación facilita el desarrollo de los proyectos a lo largo del tiempo. Tanto si el que retoma la programación es el desarrollador actual como si son otros ajenos al desarrollo original, la generación de documentación en formato HTML a partir de comentarios insertados en el código, les facilitará la comprensión de la arquitectura de la aplicación.


Si trabajamos con Atom podemos utilizar dos librerías para automatizar la generación de documentación. Instalamos en el editor el paquete "[Docblockr](https://atom.io/packages/docblockr)", que facilita comentar propiedades y métodos de nuestras clases. Por otro lado necesitamos "[Typedoc](http://typedoc.org/)" para generar la documentación, en formato HTML, a partir de los comentarios incluídos mediante "Docblockr".

{% highlight ts %}
/**
 * [HostListener description]
 * @param  {[type]} 'click'    [description]
 * @param  {[type]} ['$event'] [description]
 * @return {[type]}            [description]
 */
  @HostListener('click', ['$event']) onClick(event) {
    event.preventDefault(event);

    this.cambiaIcono();
  }
{% endhighlight %}