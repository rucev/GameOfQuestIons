# Primera Quest

Crear un programa que presente preguntas y posibles respuestas a quién vaya a jugarlo, recibiendo por input en consola la opción de la respuesta y ofreciendo feedback al respecto dependiendo de si la respuesta era correcta o incorrecta.

En pocas palabras:
* Imprimir las preguntas por consola.
* Recibir la letra de respuesta.
* Devolver un mensaje.

## Objetivos

1. Establecer la base principal de todo el juego: las preguntas.
2. Crear un primer diseño básico del juego que se ejecute en consola.
3. Tener en cuenta posibles cambios de crecimiento futuro al crear el código.

## Consejos e ideas

### JS y el input por consola

Si bien podrías plantear esta primera fase a base de alert() y prompt(), trabajar con ellos teniendo que abrir y cerrar chrome puede ser un poco tortura. Pequeño flashback sobre como trabajar en consola desde VSC.
* Ten instalado [node](https://nodejs.org/en/) y [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner).
* Mira [aquí]() la documentación de readline si necesitas refrescar. Y si no echa un vistazo a este ejemplo muy básico:

```javascript
import readline from "readline";

const getName = () => {
  const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
  });

  rl.question("¿cómo te llamas?\n", (name) => {
    console.log("Hola, "+ name)
    rl.close();
  });
};

getName();
```

### Piensa en el crecimiento del proyecto

Antes de nada, empieza trabajando con pocas preguntas, tres por ejemplo, para poder hacer pruebas rápidas.

Luego añadé más preguntas y analiza cuanto has tenido que cambiar en el código para que todo siga funcionando. Hay dos posiblidades:
1. Has cambiado unicamente la variable que almacenaba las preguntas y todo funciona. Eso es buena señal de cara a mantener el código a medida que vaya creciendo.
2. Has tenido que modificar más partes del código además de la variable que almacena las preguntas, como por ejemplo la función encargada de printearlas en consola.

Si te pasa lo segundo planteate la opción de hacerle un refactor hasta llegar al punto en que pase lo primero. Este es solo el primer paso de un proyecto más grande y todo lo que vaya a ahorrar trabajo en el futuro es buena idea. 

### Ejemplos de preguntas

A veces lo más básico resulta lo más complejo... si no se te ocurren preguntas por hacer, aquí tienes algunos ejemplos:

**¿Cuánto es 1 + 1?**
1. 2
2. 3
3. 6
4. 1

**¿A quién se refiere el nombre de Freya Stark?**
1. Un personaje de Juego de Tronos
2. Una diosa de la mitología nórdica
3. Un miembro de la familia real noruega
4. Una exploradora británica

**¿Cuál de estás palabras no es correcta según la RAE?**
1. Toballa
2. Bluyín
3. Arrascarse
4. Haiga

**¿Cuál es el gentilicio de Aguascalientes?**
1. Calentorros
2. Aguacalidenses
3. Hidrocálidos
4. Aguacalurosos

¿Qué? ¿Cuáles son las respuestas correctas? ¿Qué gracia tendría ponerlo aquí?... *aunque en el código te va a hacer falta así que toca mirar google*

## Recursos extra:
- Ten siempre a mano la [checklist](../checklist.md) de buenas prácticas.
- Si estás trabajando con tests echa un vistazo a [este repo](https://github.com/Marvalero/workshop-introduccion-al-testeo-en-javascript) y [este workshop](https://www.linkedin.com/posts/maria-valero-campa%C3%B1a_javascript-testing-escribirtests-activity-7034491159649394688-YbIi?utm_source=share&utm_medium=member_desktop).
- Ideas de cómo hacer un bucle mientras pides input al usuario en [aquí](https://github.com/rucev/LearningProjects/tree/main/JavaScript/PromisesMenu).
- Atrevéte a experimentar con los [operadores ternarios](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) en lugar de if/else demasiado cortos.

## ¿Todo listo para la siguiente quest?
[Pulsa aquí ^^](./quest2.md)