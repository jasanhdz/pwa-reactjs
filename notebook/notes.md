# Curso de Progresive Web App

Las progresive web app son el futuro de la web, no solo en tecnología sino en términos de que tan alto setean la vará de experiencia de usuario.

¿Qué es una progressive web app?

No hay una definición completa, de hecho si le preguntamos a google que son los inpulsaron está idea no tienen una definición súper comcreta, es bastante nebulosa, y creo que lo mejor es entender como es el panorama actual y comprender el problema que una PWA viene a resolver.

¿Como es la web hoy?

No es particularmente buena en mobile

- La mayoria de los usuarios ya están en mobile, mas de el 50%.
- Si pensamos en nuestros usuarios en web, una compuutadora no es párametro de lo que hacen la mayoría de nuestros usuarios, esto es muy importante en terminos de experiencia de usuario.
- Mala conexión, las conexiones 3G y LTE no son particularmente confiables
  - son lentas
  - Un sitio promedio tarda 14 segundos en cargar en un dispositivo mobil.

50% de los usuarios se van de un sitio que tarda más de 3s en cargar.
Cada segundo de demora nos cuesta un 5-10% de nuestras ventas.

**Resumen:** Una PWA es un standart de calidad, es como debería ser la web pensada primero para mobile.

**Condiciones:** Qué nuestra aplicación funcione con malas conexiones o poder agregarla como si fuera una app a la homescreem. Lo importante es que pensemos en nuestros usuarios primero, pensar en mobile, pensar en conexiones que nos son buenas, que no tienen nada que ver con entorno perfectamente y súpero hacker con el que desarrollamos nuestras aplicaciones.

## Enfoque del curso

1. Performace: ¡Mobile First! Responsive, con foco en UX
2. Instalable en la homescreen: Web Manifest, Iconos para la App.
3. Soporte Offline: Soportar malas conexiones. Confiabilidad en todo momento.

Ventajas:

Mejor experiencia de un usuario al estar en la homescreen, no hay App Stores.

## Google Lighthouse

Es una herramienta oficial de google que viene con chrome en la cual podemos hacer el diagnosticio de una PWA, esto se centra particularmente en performace y en detalles de accesibilidad, pero tiene una herramienta muy útil para testear si nuestra aplicación se considera una PWA o no y sobre todo que pasos debemos tomar para que lo sea.

## Service Workers

Un sw es lo que hace posible que las PWA funcionen, es uno de los mejores fetures que estuvo creando el equipo de chrome incluso esta disponible en safari que siempre esta muchos años atras del resto de la web, un service worker es script que nuestro navegador corre detras de escena que por defecto no tiene acceso a ninguna parte del browser, no puede tocar el dom, para eso expone una pequeña API por la que nos podemos conectar, como en el caso de recibir notificaciones, tambiéne esto significa que a los service wrokers se les puede dar mucho mayor control de lo que pasa detras de escena, podemos tener control absoluto a todo lo que sucede a nivel red.

Esto significa que podemos manejar todas las request que hace nuestro navegador y por ejemplo manejar el cache de cada una y decidir diferentes estrategias de red, como por ejemplo podemos decir que ciertas cosas deben ser cacheadas por adelantado y tener un proceso de instalación dentro de nuestra app y nos permite mejorar nuestra experiencia de usuario ya que si cargamos todo detras de escena los tiempos de carga de nuestra app van a ser muchisimo mejores, también podemos usar cosas como push notifications, donde podemos dejar a nuestro navegador detras de escena esperando a que le enviemos notificaciones como por ejemplo de los resultados de un partido de fútbol, esto significa que los service workers son los features más importantes de las PWA.
