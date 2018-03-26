# c h e s s m a p s

## What ?
chessmaps es un proyecto que nace de la mente de [Juanan](https://github.com/jamvius) :-)

En este documento README prentendo explicar el proceso mental para crear este website, siguiendo el enfoque _mobile first_, enchufando [Google Static Maps](https://developers.google.com/maps/documentation/static-maps/intro?hl=es-419#quick_example), apoyando una pata en [BootStrap 4.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/), y casi, casi hasta explicando dónde y cómo alojarlo y ponerlo en producción.

Y también me sirve como guía a mí, claro.
## Tabla de contenidos
- Mobile First
    - Lo Fundamental
    - La información
    - Estilos
    - Imágenes adaptables
    - Javascript
    - Geolocalización

- Google Static Maps

- Bootstrap

- Hosting


---

## Mobile first
Cómo crear websites que sigan el enfoque 'mobile first'?.
Piensa en webs que se adapten al tamaño de pantalla del dispositivo, pero empezando por los más pequeños.
Es decir, definir cómo despliegan la información, el diseño, y los recursos priorizando a los dispositivos móviles primero, y evolucionar a medida que la pantalla del dispositivo aumenta de tamaño.

> Mobile First, responsive, adaptive experiences.

La experiencia de usuario ideal sería adaptativa :
- **HTML** que optimice la ejecución y sea flexible,
- **CSS** que defina primero los estilos compartidos y que se vaya ampliando con _media queries_ para pantallas más grandes, ah!, y que use unidades relativas claro (ya sabes, _em, ex, ch y rem_. Todas esas maneras _raras_ de definir medidas en CSS, relativas a tamaño de fuente. O %, relativo a otro valor.).
- **Javascript** que se vaya cargando de manera condicional, en pequeños fragmentos y que utilice los eventos de pantalla (touch, swipe y todo eso).

> Fluid grids, Flexible images and Media Queries


### Lo Fundamental del "mobile first".
Primero de todo, tenemos que utilizar el viewport meta tag para definir el ancho de la pantalla a la del dispositivo.

````
<meta name="viewport" content="width=device-width, initial-scale=1" />
````


### Estructurar la información.

Lo siguiente, es pensar en incorporar la información de manera **incremental**. Empezamos con la mínima cantidad necesaria en dispositivos pequeños, y a medida que la diagonal del dispositivo crezca en tamaño, vamos incorporando el resto de partes de la información que compone la web.

> Design content-first: add information to each progressively-larger layout.

> Sort information into Primary, Secondary, Tertiary content,

En nuestro caso :
- Primary content
    - nombre (chessmaps)
    - buscador
    - mapa

- Secondary content
    - lista de resultados de búsqueda (nombre torneo, fecha, lugar)
    - lista de resultados de búsqueda en el mapa

- Tertiary content
    - buscador con filtros (distancia a mi situación actual, fechas, premios)
    - lista ampliada de resultados (ritmo de juego, premios, inscripción)
    - social links
    - otra información (bases, información adicional del torneo)

Ordered list
1. nombre
2. Buscador
3. mapa
4. resultados
5. navigation
6. social links


### Estilos.
CSS para mobile first websites = separar la hoja de estilos para pantallas más grandes.

> Write css that defines shared styles first, builds up styles for larger screens with media queries, and uses relative units,

Crear 2 archivos css, _master.css_ y _enhanced.css_ para servir estilos básicos para pantallas de menos de 40.5 em y - utilizando _media queries_ - servir estilos mejorados para pantallas más grandes de 40.5 em.

````
<link rel="stylesheet" type="text/css" href="style.css" media="screen, handheld" />
<link rel="stylesheet" type="text/css" href="enhanced.css" media="screen  and (min-width: 40.5em)" />
<!--[if (lt IE 9)&(!IEMobile)]>
<link rel="stylesheet" type="text/css" href="enhanced.css" />
<![endif]-->
````

Enchufando Bootstrap, todas estas configuraciones y ejemplos son más fluidas, y simplemente hay que utilizar su nomenclatura. Ver los [Bootstrap responsive breakpoints](https://getbootstrap.com/docs/4.0/layout/overview/#responsive-breakpoints).

### Imágenes adaptables
Optimizar las imágenes para cada dispositivo.

### Javascript
Hay que tener en cuenta que utilizamos jQuery en nuestro caso. Pero no utilizamos la librería entera.
Hay alguna manera de optimizar / recortar para tener sólo la parte que utilizamos ?. Puede que [Google Closure Compiler](https://developers.google.com/closure/compiler/?csw=1) sea una opción interesante. Elimina javascript que no utilizamos, minimiza y reescribe lo que queda de nuestras librerías / código inicial.


> Write unobtrusive Javascript to conditionally load in content fragments, take advantage of touch events and geolocation.


## Google Maps API.

 Enchufar Google Static Maps API a chessmaps.

## Bootstrap

Bootstrap puede ayudar a que todo el desarrollo vaya más rápido ???

## Cloud Hosting

### Donde lo alojamos?

En algún Cloud hosting ?
En dreamhost ?

---

#### Referencias
- [HTML 5 Rocks Responsive Design](https://www.html5rocks.com/en/mobile/responsivedesign/)
- [Google developers - Responsive Web Design](https://developers.google.com/web/fundamentals/design-and-ux/responsive/)
- [UXPin Guide to mobile first design](https://www.uxpin.com/studio/blog/a-hands-on-guide-to-mobile-first-design/)
- [Bootstrap](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
