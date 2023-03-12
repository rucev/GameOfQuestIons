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
![indent-hadouken](https://user-images.githubusercontent.com/112476868/224546111-30ec5723-1d8a-4b2f-9596-95e8c6b57e16.jpg)

Los if anidados son parte de la programación pero siempre que se pueda es mejor evitar que el código se vaya más a la derecha que... me voy a guardar las comparaciones políticas. Pero si ya has mirado la [checklist](../checklist.md) te habrás dado cuenta de que evitar dentro de lo posible los if anidados es buena práctica. ¿Por qué? Porque si se alargan mucho se vuelven algo ilegible y difícil de descifrar.

Una buena manera de prevenirlo es usando [operadores ternarios](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) pero si son algo que no te intimida o no te llama la atención siempre puedes usar otra función para prevenir que tu código se vuelva de ultraderecha.

Cojamos un ejemplo parecido al de la imagen e imaginemos que estamos comprobando si una contraseña es segura. Esta debera tener un número, una minúscula, una mayúscula y un mínimo de 6 caracteres. Para eso usariamos regex y el método test. Si no te apetece, no le des muchas vueltas y centrate solo en analizar el tema de los if anidados y si sientes curiosidad... [aquí tienes](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/RegExp/test) un poco de información sobre el tema.

Los requisitos de la contraseña en código serian:

```javascript

string.length >= 6; //Si devuelve true es porque el string tiene la longitud deseada

const hasNumbers = /\d/;   
hasNumbers.test(string);  //Si devuelve true es porque el string tiene un número

string.toLowerCase() !== string; //Si devuelve true es porque el string tiene una mayúscula

string.toUpperCase() !== string; //Si devuelve true es porque el string tiene una minúscula

```

#### 1. Comprobar la validez de la contraseña con if / else anidados

```javascript

const isPasswordValid = (password) => {
    const includesNumber = /\d/;
    if (password.length >= 6) {
        if (password.toLowerCase() !== password) {
            if (password.toUpperCase() !== password) {
                if (includesNumber.test(password)) {
                    return true;
                } else {
                    return false;
                };
            } else {
                return false;
            };
        } else {
            return false;
        };
    } else {
        return false;
    };
};

const password = "questN2";
isPasswordValid(password); // true

```

#### 2. Comprobar la validez de la contraseña con una sola condición

```javascript

const isPasswordValid = (password) => {
    const includesNumber = /\d/;
    if (password.length >= 6 && password.toLowerCase() !== password && password.toUpperCase() !== password && includesNumber.test(password)) {
        return true;
    } else {
        return false;
    }
};


const password = "questN2";
isPasswordValid(password); // true

```

#### 3. Comprobar la validez de la contraseña con un operador ternario

```javascript

const isPasswordValid = (password) => {
  const includesNumber = /\d/;
  let isPasswordValid = password.length >= 6 && password.toLowerCase() !== password && password.toUpperCase() !== password && includesNumber.test(password) ? true : false;
  return isPasswordValid;
};

const password = "questN2";
isPasswordValid(password); // true

```

#### 4. Comprobar la validez de la contraseña uniendo múltiples funciones

```javascript

const hasMinimumLength = (password) => {
    return password.length >= 6;
};

const includesLowerAndUpperCase = (password) => {
    return password.toLowerCase() !== password && password.toUpperCase() !== password;
};

const includesNumber = (password) => { 
    const includesNumber = /\d/;
    return includesNumber.test(password);
};


const isPasswordValid = (password) => {
    return hasMinimumLength(password) && includesLowerAndUpperCase(password) && includesNumber(password);
};

const password = "questN2";
isPasswordValid(password); // true

```

#### Conclusión

Seguramente se te ocurran incluso más formas de hacer lo mismo, si es el caso avísame y la añadimos ^^

Sea como sea, analicemos cada una de estas opciones. Aquí se va a juntar lo que conozco de buenas prácticas y también mi própia opinión para entender el código.

El primer ejemplo resulta confuso porque hay demasiados returns, demasiados else y puedo perder el hilo de lo que ya había comprobado antes. El segundo y el tercero, aunque tengan menos "else" y por tanto resulten más fáciles de seguir... siguen teniendo una linea muy larga que junta todas las condiciones sin dejar claro qué hace qué. No son un mal planteamiento de por sí, pero se recomiendan para condiciones más cortas y claras, en esta hay demasiados factores a tener en cuenta.

Por lo tanto mi opción favorita es la cuarta. Al separarlo todo en funciones queda claro que proposito tiene cada expresión y cuando se unen todas en una sola condición la linea no resulta demasiado larga ni confusa. Si me fuera a dormir y a la mañana siguiente mirara el código, la opción que entendería más rápido y con menor esfuerzo es la última. Esta es la idea de un código limpio.

## Recursos extra:
- Ten siempre a mano la [checklist](../checklist.md) de buenas prácticas.
- Si estás trabajando con tests echa un vistazo a [este repo](https://github.com/Marvalero/workshop-introduccion-al-testeo-en-javascript) y [este workshop](https://www.linkedin.com/posts/maria-valero-campa%C3%B1a_javascript-testing-escribirtests-activity-7034491159649394688-YbIi?utm_source=share&utm_medium=member_desktop).
- Ten en cuenta los muchos [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) de un array en JS.
- Atrevéte a experimentar con los [operadores ternarios](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) en lugar de if/else demasiado cortos.

## ¿Todo listo para la siguiente quest?
[Pulsa aquí >>](./quest3.md)

[<< Volver a la quest anterior](./quest1.md)

