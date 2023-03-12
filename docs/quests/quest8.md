# Octava Quest

Puestos a reducir el tiempo que dura el juego, vamos a añadir algo que es un clásico: tiempo limitado para responder. No vaya a ser que mientras juega alguien llame a la puerta y nuestro pobre programa se quede encendido esperando una respuesta que nunca llega [*suena música triste*](https://www.youtube.com/watch?v=jjZa3p9E_dI&ab_channel=AbrahamGalindoP.)

En pocas palabras:
* Añade un tiempo límite para responder o todas las preguntas o cada una por separado, lo que tu prefieras.
* El juego acaba si el tiempo llega a 0.

## Objetivos

1. Implementar un temporizador que puede llevar a que el juego termine incluso antes de que te quedes sin vidas o lo respondas todo bien.

## Consejos e ideas

### setTimeout

La forma más lógica de implementar esta quest es usando la función [setTimeout](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout) de Javascript.

Ten en cuenta que en dicha función se utilizan milisegundos, así que analiza el tiempo que puede tardar el usuario en leer la respuesta y deja algo de margen para responderla.

## Recursos extra:
- Ten siempre a mano la [checklist](../checklist.md) de buenas prácticas.
- Si estás trabajando con tests echa un vistazo a [este repo](https://github.com/Marvalero/workshop-introduccion-al-testeo-en-javascript) y [este workshop](https://www.linkedin.com/posts/maria-valero-campa%C3%B1a_javascript-testing-escribirtests-activity-7034491159649394688-YbIi?utm_source=share&utm_medium=member_desktop).

## ¿Todo listo para la siguiente quest?
[Pulsa aquí >>](./quest9.md)

[<< Volver a la quest anterior](./quest7.md) 