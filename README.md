# c h e s s m a p s

## What ?
chessmaps es un proyecto que nace de la mente de [Juanan](https://github.com/jamvius) :-)

En este documento README prentendo explicar el proceso mental para crear este website, siguiendo el enfoque _mobile first_, enchufando [Google Static Maps](https://developers.google.com/maps/documentation/static-maps/intro?hl=es-419#quick_example), apoyando una pata en [BootStrap 4.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/), y casi, casi hasta explicando dónde y cómo alojarlo y ponerlo en producción.

Y también me sirve como guía a mí, claro.

## Websites mobile first
Cómo crear websites que sigan el enfoque 'mobile first'?.
Piensa en webs que se adapten al tamaño de pantalla del dispositivo, pero empezando por los más pequeños.
Es decir, definir cómo despliegan la información, el diseño, y los recursos priorizando a los dispositivos móviles primero, y evolucionar a medida que la pantalla del dispositivo aumenta de tamaño.

> Mobile First, responsive, adaptive experiences.

La experiencia de usuario ideal sería adaptativa :
- **HTML** que optimice la ejecución y sea flexible,
- **CSS** que defina primero los estilos compartidos y que se vaya ampliando con _media queries_ para pantallas más grandes, ah!, y que use unidades relativas claro (ya sabes, _em, ex, ch y rem_. Todas esas maneras _raras_ de definir medidas en CSS, relativas a tamaño de fuente. O %, relativo a otro valor.).
- **Javascript** que se vaya cargando de manera condicional, en pequeños fragmentos y que utilice los eventos de pantalla (touch, swipe y todo eso).

> Fluid grids, Flexible images and Media Queries


## Lo Fundamental
Primero de todo, tenemos que utilizar el viewport meta tag para definir el ancho de la pantalla a la del dispositivo.

````
<meta name="viewport" content="width=device-width, initial-scale=1" />
````


## La información "mobile first".

Hay que pensar en incorporar la información de manera incremental. Empezamos con la minima cantidad necesaria en dispositivos pequeños, y a medida que la diagonal del dispositivo crezca en tamaño, vamos incorporando el resto de partes de la información que compone la web.

> Mobile first approach means :
> Design content-first. Add information to each progressively-larger layout,
> Sort information into Primary, Secondary, Tertiary content,
> Write css that defines shared styles first, builds up styles for larger screens with media queries, and uses relative units,
and
> Write unobtrusive Javascript to conditionally load in content fragments, take advantage of touch events and geolocation.


En nuestro caso :
### Primary content
- nombre
- buscador
- mapa

### Secondary content
- lista de resultados
- lista de resultados en el mapa
- buscador con filtros

### Tertiary content
- lista ampliada de resultados
- social links


Ordered list
1. nombre
2. Buscador
3. mapa
4. resultados
5. navigation
6. social links


## Estilos

- shared styles
- larger screens styles
  - separate style sheet for larger screens
  - mobile-first styles
- relative units



#### Referencias
[HTML 5 Rocks Responsive Design](https://www.html5rocks.com/en/mobile/responsivedesign/)
[Google developers - Responsive Web Design](https://developers.google.com/web/fundamentals/design-and-ux/responsive/)
[UXPin Guide to mobile first design](https://www.uxpin.com/studio/blog/a-hands-on-guide-to-mobile-first-design/)



## Google Maps API ??

 Enchufar Google Static Maps API a chessmaps.

## Bootstrap

Bootstrap puede ayudar a que todo el desarrollo vaya más rápido ???

## Cloud Hosting

### Donde lo alojamos?
