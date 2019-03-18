# Laboratoria JavaScript Style Guide

[Version en español](README.md)

[Versão em português](README-PT.md)

## Basic Rules

#### End each statement with a semicolon.

eslint: [semi](http://eslint.org/docs/rules/semi)

    var x = 5   // ✗ avoid
    var x = 5;  // ✓ ok

#### Use 2 spaces for indentation.

eslint: [indent](http://eslint.org/docs/rules/indent)

    // ✗ avoid
    function hello(name) {
    console.log('hi', name);
    }
    
    // ✓ ok
    function hello(name) {
      console.log('hi', name);
    }


## Function and variable names




#### Use descriptive names, in English, using camelCase.

eslint: [id-length](http://eslint.org/docs/rules/id-length)
<br>
eslint: [camelcase](http://eslint.org/docs/rules/camelcase)

    // ✗ avoid
    const OBJEcttsssss = {};
    const this_is_my_object = {};`
    const miObjecto = {};
    function c() {}
    
    // ✓ ok
    const thisIsMyObject = {};
    function thisIsMyFunction() {}


## Whitespace

### Where to add spaces

#### Add a space after keywords.

eslint: [keyword-spacing](http://eslint.org/docs/rules/keyword-spacing)

    if (condition) { ... }   // ✓ ok
    if(condition) { ... }    // ✗ avoid


#### Add spaces around operators

Except increment and decrement operators (for example, `i++` or `i--`).

eslint: [space-infix-ops](http://eslint.org/docs/rules/space-infix-ops)

    // ✗ avoid
    var x=2;
    var message = 'hello, '+name+'!';
    
    // ✓ ok
    var x = 2;
    var message = 'hello, ' + name + '!';
 

#### Add a space after commas.

Except at the end of the line.

eslint: [comma-spacing](http://eslint.org/docs/rules/comma-spacing)

    // ✓ ok
    var list = [1, 2, 3, 4];
    function greet(name, options) { ... }
    
    // ✗ avoid
    var list = [1,2,3,4];
    function greet(name,options) { ... }


#### Add  a space before blocks.

eslint: [space-before-blocks](http://eslint.org/docs/rules/space-before-blocks)

    if (admin){...}     // ✗ avoid
    if (admin) {...}    // ✓ ok

#### Add spaces inside comments.

eslint: [spaced-comment](http://eslint.org/docs/rules/spaced-comment)

    //comment           // ✗ avoid
    // comment          // ✓ ok
    
    /*comment*/         // ✗ avoid
    /* comment */       // ✓ ok


#### Add a space between colon and value in key value pairs.

eslint: [key-spacing](http://eslint.org/docs/rules/key-spacing)

    var obj = { 'key' : 'value' };    // ✗ avoid
    var obj = { 'key' :'value' };     // ✗ avoid
    var obj = { 'key':'value' };      // ✗ avoid
    
    var obj = { 'key': 'value' };     // ✓ ok


### Where not to add spaces

#### Do not use multiple spaces except for indentation.

eslint: [no-multi-spaces](http://eslint.org/docs/rules/no-multi-spaces)

    const id =    1234;    // ✗ avoid
    
    const id = 1234;       // ✓ ok


#### Do not use spaces inside parentheses.

eslint: [space-in-parens](http://eslint.org/docs/rules/space-in-parens)

    getName( name )     // ✗ avoid
    
    getName(name)       // ✓ ok


#### Do not add a space before a function declaration's parentheses.

eslint: [space-before-function-paren](http://eslint.org/docs/rules/space-before-function-paren)

    function name (arg) { ... }   // ✗ avoid
    function name(arg) { ... }    // ✓ ok
    
    run(function () { ... })      // ✗ avoid
    run(function() { ... })       // ✓ ok


#### Do not add a space between function identifiers and their invocations.

eslint: [func-call-spacing](http://eslint.org/docs/rules/func-call-spacing)

    console.log ('hello'); // ✗ avoid
    
    console.log('hello');  // ✓ ok


### How to use blank lines

#### Do not use multiple blank lines.

eslint: [no-multiple-empty-lines](http://eslint.org/docs/rules/no-multiple-empty-lines)

    // ✗ avoid 
    var value = 'hello world';


    console.log(value);
    
    // ✓ ok
    
    var value = 'hello world';
    console.log(value);


#### Do not pad within blocks.

eslint: [padded-blocks](http://eslint.org/docs/rules/padded-blocks)

    if (user) {
                               // ✗ avoid
      const name = getName();
    
    }
    
    if (user) {
      const name = getName();    // ✓ ok   
    }


## Other formatting advice

#### Use single quotes for strings.

Except when you need to use single quotes in your string.

eslint: [quotes](https://eslint.org/docs/rules/quotes)

    var str = "hi";   // ✗ avoid
    
    var str = 'hi';   // ✓ ok

#### Do not use floating decimals.

eslint: [no-floating-decimal](http://eslint.org/docs/rules/no-floating-decimal)

    const discount = .5;      // ✗ avoid
    
    const discount = 0.5;     // ✓ ok

#### Put each object property on a new line.

eslint: [object-property-newline](http://eslint.org/docs/rules/object-property-newline)

    const user = {
      name: 'Jane Doe', age: 30,
      username: 'jdoe86'            // ✗ avoid
    };
    
    const user = { name: 'Jane Doe', age: 30, username: 'jdoe86' };    // ✗ avoid
    
    const user = {
      name: 'Jane Doe',  
      age: 30,
      username: 'jdoe86' // ✓ ok
    };


#### Keep else statements on the same line as their curly braces.

eslint: [brace-style](http://eslint.org/docs/rules/brace-style)

    // ✗ avoid
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


## Best practices

#### Always use === instead of ==.

Exception: obj == null is allowed to check for null || undefined.

eslint: [eqeqeq](http://eslint.org/docs/rules/eqeqeq)

    if (name == 'John')    // ✗ avoid
    if (name === 'John')   // ✓ ok
    
    if (name != 'John')    // ✗ avoid
    if (name !== 'John')   // ✓ ok

#### Use array literals instead of array constructors.

eslint: [no-array-constructor](http://eslint.org/docs/rules/no-array-constructor)

    var nums = new Array(1, 2, 3);   // ✗ avoid
    
    var nums = [1, 2, 3];            // ✓ ok

 
