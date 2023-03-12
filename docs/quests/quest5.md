# Quinta Quest

Ha llegado el momento de complicar un poco la lógica del juego. Ahora mismo pregunta todas las preguntas de una lista así, sin más. Pero después de esta quest el programa va a tener categorías y nos hará una única pregunta aleatoria de cada categoría.

En pocas palabras:
* Añade nuevas listas de preguntas separadas por categoría.
* Elige aleatoriamente una pregunta por cada categoría.
* Si te sientes pro antes de la pregunta puedes incluir un mensaje que avise de a qué categoría pertenece.
* Termina el juego y da el feebdack en base a este nuevo diseño de partida.

## Objetivos

1. Añadir distintas categorías con múltiples preguntas.
2. Crear una función que seleccione una de esas preguntas aleatoriamente.

## Consejos e ideas

### Por dónde empezar

Antes de ponerte a crear categorías crea una función que haga una única pregunta aleatoria de las que has estado utilizando hasta el momento. Luego podrás reutilizar esa misma función para cada categoría.

### Puedes usar todos los métodos de un array para un array de objetos

A estas alturas es muy posible que ya te hayas dado cuenta. Pero por si a caso aquí tienes un pequeño ejemplo:

```javascript

const exampleQuestionArray = ["question1", "question2", "question3"];
const exampleAnswerArray = ["answer1", "answer2", "answer3"];

const exampleObjectArray = [{id: 1, question: "question1", answer:"answer1"}, {id: 2, question: "question2", answer:"answer2"}, {id: 3, question: "question3", answer:"answer3"}];

const printQuestionAndAnswer = () => {
    exampleQuestionArray.forEach(question => {
        let index = exampleQuestionArray.indexOf(question);
        console.log(question + "\n" + exampleAnswerArray[index]);
    });
};

const printButNowWithObjectArray = () => {
    exampleObjectArray.forEach(item => {
        console.log(item.question + "\n" + item.answer);
    });
};

printQuestionAndAnswer();
printButNowWithObjectArray();

// Ambas funciones printean en consola lo mismo

```

Lo único que tienes que recordar es que para acceder a cada atributo de cada objeto debes iterar la lista, si es con un forEach u otros métodos parecidos cómo has visto antes. Si no, otro ejemplo sería de la siguiente manera:

```javascript
const exampleObjectArray = [{id: 1, question: "question1", answer:"answer1"}, {id: 2, question: "question2", answer:"answer2"}, {id: 3, question: "question3", answer:"answer3"}];

const printQuestionAndAnswerWithFor = () =>{
    for(let index = 0; index < exampleObjectArray.length; index++){
        console.log(exampleObjectArray[index].question + "\n" + exampleObjectArray[index].answer);
    };
};

printQuestionAndAnswerWithFor();

// De nuevo se printea lo mismo que con el ejemplo anterior

```

### Las categorías

En el trivial clásico son historia, geografía, entretenimiento/espectáculos, arte y literatura, naturaleza y ciencias y deportes y pasatiempos. En este [link](https://psicologiaymente.com/cultura/preguntas-trivial) tienes algunos ejemplos de preguntas para cada una de estas categorías.

Pero siempre le puedes dar tu toque personal. ¿Eres muy fan de nintendo? Pues tus categorías pueden ser pokémon, zelda, mario, metroid y kirby. ¿Eres más de series? haz una categoría por cada una de tus cinco series favoritas. Si lo haces sobre algo que a ti te encante siempre es más divertido que tirar por lo génerico, sobretodo mientras hagas pruebas para ver si funciona. Eso sí, también supone dedicarle más tiempo.

## Recursos extra:
- Ten siempre a mano la [checklist](../checklist.md) de buenas prácticas.
- Si estás trabajando con tests echa un vistazo a [este repo](https://github.com/Marvalero/workshop-introduccion-al-testeo-en-javascript) y [este workshop](https://www.linkedin.com/posts/maria-valero-campa%C3%B1a_javascript-testing-escribirtests-activity-7034491159649394688-YbIi?utm_source=share&utm_medium=member_desktop).
- Ten en cuenta los muchos [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) de un array en JS.

## ¿Todo listo para la siguiente quest?
[Pulsa aquí >>](./quest6.md)

[<< Volver a la quest anterior](./quest4.md)