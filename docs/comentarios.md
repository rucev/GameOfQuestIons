# Comentarios:

Siguiendo el libro de [Clean Code](https://www.amazon.es/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882/ref=sr_1_1?adgrpid=61918603091&gclid=Cj0KCQiA6rCgBhDVARIsAK1kGPIMM6kdF35s37VHxQcXlKVyBrec3qLSXPJ2LZa5NCZztwE_fqNLOCkaAuwUEALw_wcB&hvadid=275464920674&hvdev=c&hvlocphy=1005414&hvnetw=g&hvqmt=e&hvrand=17940655800515023316&hvtargid=kwd-301191331858&hydadcr=23858_1824318&keywords=clean+code&qid=1678554587&sr=8-1), vamos a darle una vuelta a los comentarios y su buen uso.

La principal razón para usar comentarios es que haya **algo que no podamos expresar con el código**. Aún así, es importante tener presente que un mal código con muchos comentarios es mucho más confuso que un código limpio, con los comentarios justos y necesarios. Es decir, **evita usar comentarios si puedes escribirlo en una función o una variable**.

### Ejemplo de comentario mal planteado

```javascript
// Check if match is over:
if(questions.every((question) => questions.isDone === true)) {
	console.log("game over");
}
```

### Ejemplo de código limpio, sin el comentario
```javascript
const isMatchOver = () => {
    return (questions.every((question) => questions.isDone === true));
}
if(isMatchOver()) {
    console.log("game over"); 
}
```

## Comentarios considerados apropiados en un código limpio:

*	**Comentarios legales**: copyright y cosas así.
*	**Comentarios informativos**: por ejemplo, si vamos a usar regex para algo, podemos poner un ejemplo de que expresión se trata.
*	**Explicar la intención**: en caso de que no esta clara en el código porque aun no se usa o se prevee que se use en el futuro.
*	**TODO**: comentarios que marcan cosas por hacer, de hecho hay extensiones chulas que recomiendo para estos en VSC como [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree) y [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree).
*	**Amplificaciones** *traducción del inglés debatible por mi parte*: sirven para resaltar la importancia de algo que puede parecer innecesario a simple vista. Por ejemplo el siguiente comentario en una función que añade 0 al numero de los primeros 9 meses del año:

```javascript
//Adding this 0 to the Date is important so all the months have the same format)
```

## Comentarios que ensucian el código:

*	**Información incorrecta**: decir que algo devuelve false cuando devuelve 0, por ejemplo.
*	**Comentarios de diario**:

```javascript
/*hoy he hecho esto, esto y esto, mañana quiero hacer esto otro, y lo otro y lo otro de lo otro…*/
```

La idea del código limpio es **que lo que has hecho hoy se entienda a simple vista**, y si no es el caso, **escribe un TODO** sobre porqué y como debes corregirlo.

*	**Ruido**: comentarios que solo sirven para insistir en lo obvio. Recuperando el ejemplo anterior, la función tiene un nombre suficientemente descriptivo, no necesita un comentario:

```javascript
// Check if match is over:
const isMatchOver = () => {
    return (questions.every((question) => questions.isDone === true));
}
```

*	**Titulos de funciones**: bastante relacionado con el anterior. La función debe tener un nombre autoexplicativo, no un comentario explicándola.
*	**Marcadores de posición**: subtitulos dentro del código como por ejemplo:

```javascript
//Setting questions tools.
```

Si tu código es tan largo que merece dividirse en subtitulos… es mejor practica separarlo en varios archivos e ir importándolos.

*	**Firmas atributivas**: Si estas trabajando en grupo este registro ya lo tiene git… ¿no?. No lo metas en tu código.

```javascript
/*Added by Flors*/
```

*	**Codigo *no utilizado* comentado**:
1. Si esta comentado nadie se atreverá a eliminarlo por si hace falta, pero si no hace falta sobra, y si hace falta en ese momento... ¿qué hace comentado?
2. Teniendo eso en cuenta... si sobra quítalo.
3. Y si se va a usar en un futuro pero ahora no, mete un TODO.
