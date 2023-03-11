Comentarios:
La principal razón para usar comentarios es que haya algo que no podamos expresar con el código. Un mal código con muchos comentarios es más confuso que un código limpio, con los comentarios justos y necesarios. Es decir, evita usar comentarios si puedes escribirlo en una función o una variable.
Ejemplo:
1.	NOPE
```javascript
// Check if match is over:
if(questions.every((question) => questions.isDone === true)) {
	console.log("game over");
}
```
2.	SIP
```javascript
const isMatchOver = () => {
    return (questions.every((question) => questions.isDone === true));
}
if(isMatchOver()) {
    console.log("game over"); 
}
```
Comentarios considerados apropiados:
-	Comentarios legales (copyright y cosas así)
-	Comentarios informativos (si vamos a usar regex para algo, podemos poner un ejemplo de que expresión se trata).
-	Explicar la intención (si no esta clara en el código porque aun no se usa o se prevee que se use en el futuro, por ejemplo)
-	TODO (cosas por hacer, de hecho hay extensiones chulas para estos en VSC. Dos ejemplos: …, …)
-	Amplificaciones: para resaltar la importancia de algo que puede parecer innecesario a simple vista (ej en una función que añade 0 al numero de los primeros 9 meses del año: //Adding this 0 to the Date is important so all the months have the same format)
Comentarios que se considera que sobran:
-	Información incorrecta: (decir que algo devuelve false cuando devuelve 0, por ejemplo)
-	Comentarios de diario (hoy he hecho esto, esto y esto, mañana quiero hacer esto… la idea del código limpio es que lo que has hecho hoy se entienda a simple vista, y si no es el caso, escribe un TODO sobre como debes corregirlo).
-	Ruido (comentarios que solo sirven para insistir en lo obvio). Recuperando el ejemplo anterior:
```javascript
// Check if match is over:
const isMatchOver = () => {
    return (questions.every((question) => questions.isDone === true));
}
```
-	Titulos de funciones: bastante relacionado con el anterior. La función debe tener un nombre autoexplicativo,
-	Marcadores de posición (subtitulos dentro del código en plan //Setting questions tolos. Si tu código es tan largo que merece dividirse en subtitulos… es mejor practica separarlo en varios archivos e ir importándolos).
-	Firmas atributivas (por ejemplo : /*Added by Flors*/). Si estas trabajando en grupo este registro ya lo tiene git… no? 
-	Codigo “no utilizado” comentado: si esta comentado nadie se atreverá a eliminarlo por si hace falta… si sobra quítalo, si se va a usar en un futuro pero ahora no mete un TODO.
