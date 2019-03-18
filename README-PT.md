# Guia de Estilo de JavaScript

[Versão em inglês](README-EN.md)

## Regras Básicas

#### Finalizar cada instrução con ponto e vírgula.
***End each statement with a semicolon.***

eslint: [semi](http://eslint.org/docs/rules/semi)

    var x = 5   // ✗ evitar
    var x = 5;  // ✓ ok

#### Utilizar dois espaços para indentação.
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


## **Nomes de variáveis e funções**




#### Use nomes descritivos em inglês e no formato camelCase.
***Use descriptive names, in English, using camelCase.***

eslint: [id-length](http://eslint.org/docs/rules/id-length)
<br>
eslint: [camelcase](http://eslint.org/docs/rules/camelcase)

    // ✗ evitar
    const OBJEcttsssss = {};
    const this_is_my_object = {};
    const miObjecto = {};
    function c() {}
    
    // ✓ ok
    const thisIsMyObject = {};
    function thisIsMyFunction() {}


## Uso de espaços em branco

### Onde adicionar espaços

#### Adicionar um espaço após as palavras-chave.
***Add a space after keywords.***

eslint: [keyword-spacing](http://eslint.org/docs/rules/keyword-spacing)

    if (condition) { ... }   // ✓ ok
    if(condition) { ... }    // ✗ evitar


#### Adicionar espaços em cada lado dos operadores.
***Add spaces around operators***

Exceto os operadores de incremento e decremento (por exemplo, `i++` ou `i--`).
<br>
*Except increment and decrement operators (for example, `i++` or `i--`).*

eslint: [space-infix-ops](http://eslint.org/docs/rules/space-infix-ops)

    // ✗ evitar
    var x=2;
    var message = 'hello, '+name+'!';
    
    // ✓ ok
    var x = 2;
    var message = 'hello, ' + name + '!';
 

#### Adicionar um espaço após as vírgulas.
***Add a space after commas.***

Exceto no caso do último caracter da linha.
<br>
*Except at the end of the line.*

eslint: [comma-spacing](http://eslint.org/docs/rules/comma-spacing)

    // ✓ ok
    var list = [1, 2, 3, 4];
    function greet(name, options) { ... }
    
    // ✗ evitar
    var list = [1,2,3,4];
    function greet(name,options) { ... }


#### Adicionar um espaço antes dos blocos.
***Add  a space before blocks.***

eslint: [space-before-blocks](http://eslint.org/docs/rules/space-before-blocks)

    if (admin){...}     // ✗ evitar
    if (admin) {...}    // ✓ ok

#### Usar espaços dentro dos comentários
<br>
***Add spaces inside comments.***

eslint: [spaced-comment](http://eslint.org/docs/rules/spaced-comment)

    //comment           // ✗ evitar
    // comment          // ✓ ok
    
    /*comment*/         // ✗ evitar
    /* comment */       // ✓ ok


#### Adicionar um espaço entre os dois pontos e o valor da chave.
***Add a space between colon and value in key value pairs.***

eslint: [key-spacing](http://eslint.org/docs/rules/key-spacing)

    var obj = { 'key' : 'value' };    // ✗ evitar
    var obj = { 'key' :'value' };     // ✗ evitar
    var obj = { 'key':'value' };      // ✗ evitar
    
    var obj = { 'key': 'value' };     // ✓ ok


### **Onde não adicionar espaços**

#### Evitar uso de múltiplos espaços em branco, exceto na indentação.
***Do not use multiple spaces except for indentation.***

eslint: [no-multi-spaces](http://eslint.org/docs/rules/no-multi-spaces)

    const id =    1234;    // ✗ evitar
    
    const id = 1234;       // ✓ ok


#### Evitar espaços em branco dentro de parênteses.
***Do not use spaces inside parentheses.***

eslint: [space-in-parens](http://eslint.org/docs/rules/space-in-parens)

    getName( name )     // ✗ evitar
    
    getName(name)       // ✓ ok


#### Evitar uso de espaço entre a declaração da função e os parênteses.
***Do not add a space before a function declaration's parentheses.***

eslint: [space-before-function-paren](http://eslint.org/docs/rules/space-before-function-paren)

    function name (arg) { ... }   // ✗ evitar
    function name(arg) { ... }    // ✓ ok
    
    run(function () { ... })      // ✗ evitar
    run(function() { ... })       // ✓ ok


#### Evitar espaçoes entre o identificador da função e sua chamada.
***Do not add a space between function identifiers and their invocations.***

eslint: [func-call-spacing](http://eslint.org/docs/rules/func-call-spacing)

    console.log ('hello'); // ✗ evitar
    
    console.log('hello');  // ✓ ok


### **Como usar linhas em branco**

#### Não use múltiplas linhas em branco.
***Do not use multiple blank lines.***

eslint: [no-multiple-empty-lines](http://eslint.org/docs/rules/no-multiple-empty-lines)

    // ✗ evitar 
    var value = 'hello world';


    console.log(value);
    
    // ✓ ok
    
    var value = 'hello world';
    console.log(value);


#### Não use linhas em branco dentro dos blocos.
***Do not pad within blocks.***

eslint: [padded-blocks](http://eslint.org/docs/rules/padded-blocks)

    if (user) {
                               // ✗ evitar
      const name = getName();
    
    }
    
    if (user) {
      const name = getName();    // ✓ ok
    }


## **Outros tópicos de formato**

#### Usar aspas simples para strings.
***Use single quotes for strings.***

Exceto quando for necessário usar aspas em um texto.
<br>
*Except when you need to use single quotes in your string.*

eslint: [quotes](https://eslint.org/docs/rules/quotes)

    var str = "hi";   // ✗ evitar
    
    var str = 'hi';   // ✓ ok

#### Não usar pontos flutuantes como decimais.
***Do not use floating decimals.***

eslint: [no-floating-decimal](http://eslint.org/docs/rules/no-floating-decimal)

    const discount = .5;      // ✗ evitar
    
    const discount = 0.5;     // ✓ ok

#### Declarar cada propriedade de um objeto por linha.
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


#### Manter a declaração *else* na mesma linha das chaves.
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


## Boas práticas

#### Usar sempre === em vez de ==.
***Always use === instead of ==.***

Com exceção de == null para verificar se o objeto é null || undefined.
<br>
*Exception: obj == null is allowed to check for null || undefined.*

eslint: [eqeqeq](http://eslint.org/docs/rules/eqeqeq)

    if (name == 'John')    // ✗ evitar
    if (name === 'John')   // ✓ ok
    
    if (name != 'John')    // ✗ evitar
    if (name !== 'John')   // ✓ ok

#### Usar array literal ao invés de array constructors.
**Use array literals instead of array constructors.**

eslint: [no-array-constructor](http://eslint.org/docs/rules/no-array-constructor)

    var nums = new Array(1, 2, 3);   // ✗ evitar
    
    var nums = [1, 2, 3];            // ✓ ok

 

