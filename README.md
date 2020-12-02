# Una Guía de Estilo de JavaScript

:warning: Este repositorio ha sido DEPRECADO en favor de
[`airbnb/javascript`](https://github.com/airbnb/javascript).

***

[Version en inglés](README-EN.md)

[Version en portugués](README-PT.md)

## Reglas Básicas

#### Termina cada instrucción con punto y coma.
***End each statement with a semicolon.***

eslint: [semi](http://eslint.org/docs/rules/semi)

    var x = 5   // ✗ evitar
    var x = 5;  // ✓ ok

#### Usa 2 espacios como indentación.
***Use 2 spaces for indentation.***

eslint: [indent](http://eslint.org/docs/rules/indent)

    // ✗ evitar
    function hello(name) {
    console.log('hi', name);
    }

    // ✓ ok
    function hello(name) {
      console.log('hi', name);
    }


## **Nombres de variables y funciones**




#### Usa nombres descriptivos en Inglés y en el formato camelCase.
***Use descriptive names, in English, using camelCase.***

eslint: [id-length](http://eslint.org/docs/rules/id-length)
<br>
eslint: [camelcase](http://eslint.org/docs/rules/camelcase)

    // ✗ evitar
    const OBJEcttsssss = {};
    const this_is_my_object = {};`
    const miObjecto = {};
    function c() {}

    // ✓ ok
    const thisIsMyObject = {};
    function thisIsMyFunction() {}


## Uso de espacios en blanco

### Donde agregar espacios

#### Agrega un espacio después de las palabras claves.
***Add a space after keywords.***

eslint: [keyword-spacing](http://eslint.org/docs/rules/keyword-spacing)

    if (condition) { ... }   // ✓ ok
    if(condition) { ... }    // ✗ evitar


#### Agrega espacios a cada lado de los operadores.
***Add spaces around operators***

Con la excepción de los operadores de incremento y decremento (por ejemplo, `i++` o `i--`).
<br>
*Except increment and decrement operators (for example, `i++` or `i--`).*

eslint: [space-infix-ops](http://eslint.org/docs/rules/space-infix-ops)

    // ✗ evitar
    var x=2;
    var message = 'hello, '+name+'!';

    // ✓ ok
    var x = 2;
    var message = 'hello, ' + name + '!';


#### Agrega un espacio después de las comas.
***Add a space after commas.***

Excepto si es el último símbolo en la línea.
<br>
*Except at the end of the line.*

eslint: [comma-spacing](http://eslint.org/docs/rules/comma-spacing)

    // ✓ ok
    var list = [1, 2, 3, 4];
    function greet(name, options) { ... }

    // ✗ evitar
    var list = [1,2,3,4];
    function greet(name,options) { ... }


#### Agrega un espacio antes de los bloques.
***Add  a space before blocks.***

eslint: [space-before-blocks](http://eslint.org/docs/rules/space-before-blocks)

    if (admin){...}     // ✗ evitar
    if (admin) {...}    // ✓ ok

#### Usar espacios dentro de comentarios.
<br>
***Add spaces inside comments.***

eslint: [spaced-comment](http://eslint.org/docs/rules/spaced-comment)

    //comment           // ✗ evitar
    // comment          // ✓ ok

    /*comment*/         // ✗ evitar
    /* comment */       // ✓ ok


#### Agregar un espacio entre dos puntos y pares clave valor.
***Add a space between colon and value in key value pairs.***

eslint: [key-spacing](http://eslint.org/docs/rules/key-spacing)

    var obj = { 'key' : 'value' };    // ✗ evitar
    var obj = { 'key' :'value' };     // ✗ evitar
    var obj = { 'key':'value' };      // ✗ evitar

    var obj = { 'key': 'value' };     // ✓ ok


### **Donde no agregar espacios**

#### Evita el uso de espacios en blanco múltiples a excepción de indentación.
***Do not use multiple spaces except for indentation.***

eslint: [no-multi-spaces](http://eslint.org/docs/rules/no-multi-spaces)

    const id =    1234;    // ✗ evitar

    const id = 1234;       // ✓ ok


#### Evita espacios en blanco entre paréntesis.
***Do not use spaces inside parentheses.***

eslint: [space-in-parens](http://eslint.org/docs/rules/space-in-parens)

    getName( name )     // ✗ evitar

    getName(name)       // ✓ ok


#### Evita uso de espacios antes de los paréntesis de la función declarada.
***Do not add a space before a function declaration's parentheses.***

eslint: [space-before-function-paren](http://eslint.org/docs/rules/space-before-function-paren)

    function name (arg) { ... }   // ✗ evitar
    function name(arg) { ... }    // ✓ ok

    run(function () { ... })      // ✗ evitar
    run(function() { ... })       // ✓ ok


#### Evita uso de espacios entre el identificador de la función y su invocación.
***Do not add a space between function identifiers and their invocations.***

eslint: [func-call-spacing](http://eslint.org/docs/rules/func-call-spacing)

    console.log ('hello'); // ✗ evitar

    console.log('hello');  // ✓ ok


### **Cómo usar líneas en blanco**

#### No usa múltiples líneas en blanco.
***Do not use multiple blank lines.***

eslint: [no-multiple-empty-lines](http://eslint.org/docs/rules/no-multiple-empty-lines)

    // ✗ evitar
    var value = 'hello world';


    console.log(value);

    // ✓ ok

    var value = 'hello world';
    console.log(value);


#### No usa líneas en blanco de relleno entre bloques.
***Do not pad within blocks.***

eslint: [padded-blocks](http://eslint.org/docs/rules/padded-blocks)

    if (user) {
                               // ✗ evitar
      const name = getName();

    }

    if (user) {
      const name = getName();    // ✓ ok
    }


## **Otros consejos de formato**

#### Usar comillas simples en cadenas de texto.
***Use single quotes for strings.***

Con la excepción para evitar escapado de texto.
<br>
*Except when you need to use single quotes in your string.*

eslint: [quotes](https://eslint.org/docs/rules/quotes)

    var str = "hi";   // ✗ evitar

    var str = 'hi';   // ✓ ok

#### Evitar puntos decimales flotantes.
***Do not use floating decimals.***

eslint: [no-floating-decimal](http://eslint.org/docs/rules/no-floating-decimal)

    const discount = .5;      // ✗ evitar

    const discount = 0.5;     // ✓ ok

#### Mantener consistencia de declarar propiedades de un objeto por línea.
***Put each object property on a new line.***

eslint: [object-property-newline](http://eslint.org/docs/rules/object-property-newline)

    const user = {
      name: 'Jane Doe', age: 30,
      username: 'jdoe86'            // ✗ evitar
    };

    const user = { name: 'Jane Doe', age: 30, username: 'jdoe86' };    // ✗ evitar

    const user = {
      name: 'Jane Doe',
      age: 30,
      username: 'jdoe86' // ✓ ok
    };


#### Mantener la declaración *else* en la misma línea que sus llaves.
***Keep else statements on the same line as their curly braces.***

eslint: [brace-style](http://eslint.org/docs/rules/brace-style)

    // ✗ evitar
    if (condition) {
     // ...
    }
    else {
     // ...
    }

    // ✓ ok
    if (condition) {
     // ...
    } else {
     // ...
    }


## Buenas prácticas

#### Usa siempre === en vez de ==.
***Always use === instead of ==.***

Con la excepción de obj == null para verificar si el objeto sea null || undefined.
<br>
*Exception: obj == null is allowed to check for null || undefined.*

eslint: [eqeqeq](http://eslint.org/docs/rules/eqeqeq)

    if (name == 'John')    // ✗ evitar
    if (name === 'John')   // ✓ ok

    if (name != 'John')    // ✗ evitar
    if (name !== 'John')   // ✓ ok

#### Usa array literales en vez de array constructors.
**Use array literals instead of array constructors.**

eslint: [no-array-constructor](http://eslint.org/docs/rules/no-array-constructor)

    var nums = new Array(1, 2, 3);   // ✗ evitar

    var nums = [1, 2, 3];            // ✓ ok



