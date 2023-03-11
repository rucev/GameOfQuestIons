# Segunda Quest

Si te has tomado muy en serio la primera quest puede que ya hayas contemplado o incluso hecho la segunda. Se trata de añadir control de errores ante inputs no válidos. Las opciones son 1, 2, 3 o 4. Tal vez A, B, C o D. ¿Qué pasa si alguien pulsa y envía una letra que no es? ¿Y si es una letra en minúscula en lugar de la mayúscula? ¿Es un error igual de grave?

Como lo plantees es cosa tuya, pero en esta quest tienes que controlar las idas de olla que quien esté jugando escriba en la consola para que no se rompa todo y luego volver a plantearle la pregunta, a ver si a la segunda es menos cabeza hueca y le da a una opción válida.

En pocas palabras:
* Ante un input erroneo evita que dé un fallo el programa.
* Envía un mensaje informando del error al usuario.
* Devolver la misma pregunta hasta que le de a una respuesta válida (ya sea correcta o incorrecta)

## Objetivos

1. Evitar fallos por consola.
2. Permitir que el juego siga pese a ofrecer un input no aceptado.


## Consejos e ideas

### if anidados
Los if anidados son parte de la programación pero siempre que se pueda es mejor evitar que el código se vaya más a la derecha que... me voy a guardar las comparaciones políticas.

Una buena manera de prevenirlo es usando [operadores ternarios](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) pero si son algo que no te intimida o no te llama la atención siempre puedes usar otra función para prevenir que tu código se vuelva de ultraderecha.

#### if / else anidados


## Recursos extra:
- Ten siempre a mano la [checklist](../checklist.md) de buenas prácticas.
- Si estás trabajando con tests echa un vistazo a [este repo](https://github.com/Marvalero/workshop-introduccion-al-testeo-en-javascript) y [este workshop](https://www.linkedin.com/posts/maria-valero-campa%C3%B1a_javascript-testing-escribirtests-activity-7034491159649394688-YbIi?utm_source=share&utm_medium=member_desktop).
- Ten en cuenta los muchos [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) de un array en JS.
- Atrevéte a experimentar con los [operadores ternarios](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) en lugar de if/else demasiado cortos.

## ¿Todo listo para la siguiente quest?
[Pulsa aquí ^^](./quest3.md)

