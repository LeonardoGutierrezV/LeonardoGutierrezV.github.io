---
layout: single
title: ¿Qué es Markdown?
excerpt: "Explicación rápida sobre que es y para que sirve markdown."
date: 2021-11-04
classes: wide
header:
  teaser: /assets/images/2021-11-04-que-es-markdown/logo.png
  teaser_home_page: true
  icon: /assets/images/www_icon.png
categories:
  - Markdown
  - Diseño web
tags:
  - Markdown
  - Web
  - Guía
---

## Markdown
Markdown es un lenguaje de marcado que fue creado por John Gruber y Aaron Swartz en 2004 y se distribuye de forma gratuita bajo un licenciamiento BSD, este nació como una herramienta de conversión de texto plano a HTML y su función principal es simplificar la escritura de documentos o páginas web.

Este documento pretende realizar una explicación simple sencilla y práctica sobre Markdown, con la intención de puedas utilizarlo de manera fácil en tus publicaciones.

## Elementos básicos de Markdown

### Encabezados
Para crear encabezados utilice el simbolo de almoadilla (#)al principio de una línea.

vea los siguientes ejemplos.

```
# Mi primer título.
```
# Mi primer título sencillo.

```
## Mi primer título con decorado
```
## Mi primer título con decorado.

Si utilizamos tres signos # el documento lo interpretara como la inserción de un subtitulo.

```
### Un nuevo subtitulo.
```
### Un nuevo subtitulo.

```
#### Un nuevo subtitulo nivel 4.
##### Un nuevo subtitulo nivel 5.
###### Un nuevo subtitulo nivel 6.
```

#### Un nuevo subtitulo nivel 4.
##### Un nuevo subtitulo nivel 5.
###### Un nuevo subtitulo nivel 6.

De 4 a 6 almohadillas el subtítulo simplemente reducirá su tamaño.

### Texto básico.

Cuando se requiere dar formato al texto de un párrafo no se requiere sintaxis especializada.

```
Letra en **negrita**.
```
 
Letra en **negrita**.

```
Letra **cursiva**.
```

Letra **cursiva**.

```
Letra ***negrita y cursiva***.
```

Letra ***negrita y cursiva***.

### Listas numeradas y listas con viñetas.

Para una lista numerada basta con escribir una lista comenzando cada línea con un numero seguida de “.” y separando el identificador con un espacio.

```
1. Uno
2. Dos
3. Tres
20. veinte.
30. Treinta
```
1. Uno
2. Dos
3. Tres
20. veinte.
30. Treinta

Para crear una lista con viñetas puede comenzar la línea con alguno de los siguientes signos. * - +

```
* Viñeta *
* Viñeta *

- Viñeta -
- Viñeta -

+ Viñeta +
+ Viñeta +
```

* Viñeta *
* Viñeta *

- Viñeta -
- Viñeta -

+ Viñeta +
+ Viñeta +

Se puede también anidar listas utilizando una tabulación de 4 espacios para generar un diferenciador entre cada sección de las listas anidadas.

```
* Viñeta *
    - Viñeta -
      + Viñeta +
* Viñeta *
    - Viñeta -
        + Viñeta +
```

* Viñeta *
    - Viñeta -
      + Viñeta +
* Viñeta *
    - Viñeta -
        + Viñeta +

## Elementos de bloque

Para generar un nuevo párrafo en Markdown basta con separar el texto con una línea en blanco. De la misma forma que sucede con HTML Markdown no soporta dobles líneas en blanco de tal forma que al detectar dos líneas en blanco las convertirá en una.Para realizar un **salto de línea y empezar una frase en una línea** siguiente dentro del mismo párrafo, **tendrás que pulsar dos veces la barra espaciadora antes de pulsar una vez enter.**

### Citas.

Para generar una cita en un documento Markdown basta con iniciar tu texto con el signo mayor que.

```
> “El que se encadena a una alegría, destruye una vida libre; pero el que besa la alegría en su vuelo, vive el amanecer de la eternidad.”
- William Blake
```
> “El que se encadena a una alegría, destruye una vida libre; pero el que besa la alegría en su vuelo, vive el amanecer de la eternidad.” - William Blake

Puedes incluso generar citas anidadas de la siguiente forma.

```
> cita primaria 
>> cita secundaría
```

> cita primaria 
>> cita secundaría

### Codigos de bloque.

Markdown nos facilita la inclusión de código, dicho código debe estar escrito entre dos líneas compuestas por tres varguillas ~~~.

```
~~~
print("hellow world!")
~~~
```

~~~
print("hellow world!")
~~~

Podemos tambien incluir bloques de codigo de algunos lenguajes de programación o lenguajes de marcado.

~~~
```python 
your_code = do_some_stuff
print("hellow world!")
```
~~~


```python 
your_code = do_some_stuff
print("hellow world!")
```


### Sintaxis soportada por Markdown

| actionscript3 | csv | make - Makefile | sql |
| apache | bash | markdown | svg |
| applescript | diff | matlab | swift |
| asp | elixir | nginx | rb, jruby, ruby - Ruby |
| brainfuck | erb - HTML + Embedded Ruby | objectivec | smalltalk |
| c | go | pascal | vim, viml - Vim Script |
| cfm | haml | PHP | volt |
| clojure | http | Perl | vhdl |
| cmake | java | python | vue |
| coffee-script, coffeescript, coffee | javascript | profile - python profiler output | xml - XML and also used for HTML with inline CSS and Javascript |
| cpp - C++ | json | rust | yaml |
| cs | jsx | salt, saltstate - Salt |  |
| csharp | less | shell, sh, zsh, bash - Shell scripting |  |
| css | lolcode | scss |  |

### Reglas horizontales.

Una manera de separar de forma visual los elementos de un documento en Markdown es con las reglas horizontales, para lo cual hacemos uso de: asteriscos, guiones bajos ó guiones.  
Como se muestra a continuación.

```
***
```
***

```
---
```
---

```
---
```
---

## Elementos de línea.

Los elementos de línea nos permiten dar funcionalidad adicional a nuestro documento de Markdown.

## Links

Es el elemento mas comun para poder vincular paginas documentos, archivos y cualquier otro recurso que necesitamos compartir si integrarlo directamente al documento.

```
[Acceso a github](https://github.com)
```

[Acceso a github](https://github.com)

hipervinculo directo.

```
<https://github.com>
```

<https://github.com>


### Código

Puedes tambien insertar lineas simples de codigo de la siguente manera:


```
Codigo para ejecutar ping: `ping 192.168.1.1`
```

Codigo para ejecutar ping: `ping 192.168.1.1`

### Imágenes

Para agregar imagenes puedes hacerlo de la siguiente manera.

```
![Mi primera imagen](https://i.imgur.com/vIvB8GV.png)
```

![Mi primera imagen](https://i.imgur.com/vIvB8GV.png)

![Mi segunda imagen](https://fleep.io/blog/wp-content/uploads/2014/07/github_icon.png "Logo")


### Tablas

Es facil incluir tablas en Markdown a nuestros documentos utilizando los siguientes separadores.

~~~
| Nacionalidad | País | Idioma |
|--- |--- |--- |
| Dutch (holandesa) | Netherlands (Países Bajos) | Dutch (holandés)| 
| American (estadounidense) | United States (Estados Unidos) | English (inglés) |
| Canadian (canadiense) | Canada (Canadá) | English/French (inglés/francés) |
| Mexican (mexicana) | Mexico (Mexico) | Spanish (español) |
~~~


| Nacionalidad | País | Idioma |
|--- |--- |--- |
| Dutch (holandesa) | Netherlands (Países Bajos) | Dutch (holandés)| 
| American (estadounidense) | United States (Estados Unidos) | English (inglés) |
| Canadian (canadiense) | Canada (Canadá) | English/French (inglés/francés) |
| Mexican (mexicana) | Mexico (Mexico) | Spanish (español) |

Con el contenido revisado en esta publicación, ya podrás construir de manera fácil y sencilla documentación utilizando Markdown y simplificando el proceso.