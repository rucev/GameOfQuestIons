# Checklist de buenas prácticas:

- [ ] Naming descriptivo y en inglés.

- [ ] No usar en el nombre unicamente el tipo de valor que es (array, object, etc).

- [ ] Uso de let/const (var esta pasado de moda). Y siempre que se pueda priorizar const por encima de let.

- [ ] Las funciones deben empezar por un verbo (posteriormente puede incluir nombres: setName, getQuestions, etc).

- [ ] Evitar abreviaturas en el naming.

- [ ] Usar arrow functions (en lugar de definir las funciones con function).

- [ ] No declarar una función dentro de otra, para eso es mejor usar clases.

- [ ] Dividirlo todo en funciones chiquitas, luego llamar una única que lo ejecute todo si es el caso.

- [ ] Separar las funciones con espacios.

- [ ] Evitar el uso de loose equality (==).

- [ ] El break dentro del if es mala practica (mejor usar un return si eso).

- [ ] Código excesivamente indentado: si ves que se va todo muy a la derecha es mejor romperlo en funciones o plantearlo de otra manera. Revisa esta [quest](./quests/quest2.md) para saber más.

- [ ] En una función, intentar que, si hay más de un return, devuelva siempre el mismo tipo de variable.

- [ ] Más líneas de código no significan mejor código (aunque Elon Musk opine lo contrario…).

- [ ] Los comentarios son un arma de doble filo, revisa esta [documentación](./comentarios.md) sobre el tema.

- [ ] En html evitar el uso de id (mucho mejor usar class).




Para ir marcando los checks edita el documento y pon una "[ x ]" entre los corchetes.




**¡La idea es que del código limpio es que sea lo más fácil de entender y legible posible!**




**Siguiendo la información de [Clean Code](https://www.amazon.es/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882/ref=sr_1_1?adgrpid=61918603091&gclid=Cj0KCQiA6rCgBhDVARIsAK1kGPIMM6kdF35s37VHxQcXlKVyBrec3qLSXPJ2LZa5NCZztwE_fqNLOCkaAuwUEALw_wcB&hvadid=275464920674&hvdev=c&hvlocphy=1005414&hvnetw=g&hvqmt=e&hvrand=17940655800515023316&hvtargid=kwd-301191331858&hydadcr=23858_1824318&keywords=clean+code&qid=1678554587&sr=8-1) y lo que estoy aprendiendo en el bootcamp de [ISDI](https://isdicoders.com/).*