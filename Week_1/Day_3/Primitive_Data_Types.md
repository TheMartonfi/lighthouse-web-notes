## The Six Primitive Types in JavaScript
Primitives are `essential` building blocks of data because they represent the `simplest possible type` of data that our software can have.

The `six` types of primitives:
* undefined
* null
* boolean
* string
* number
* symbol (Introduced in ES6)

## Primitive Types Don't Have Properties

Each primitive (excluding symbol which has weird rules) has a corresponding object constructor; you can see this clearly in the following example:

```javascript
typeof(true); 
// "boolean" 
typeof(Boolean(true)); 
// => "boolean" 
typeof(new Boolean(true));
// => "object"
/*  
  It is generally considered bad practice to use primitive object constructors (as shown in the final line above). 
*/
```

An `object constructor` can be invoked with the word `new`, as seen above. Each object has `methods` associated with them based on what `constructor` was used.

As stated above, `primitive data types do not have properties`. So why exactly does "someString".length work? Let's take you back to the behaviour of == vs ===. When you use ==, JavaScript does this fun thing called `type coercion`. This means that JavaScript will take `different data types`, and one of them will be converted to an `"equivalent"`. A good example of this is:

```javascript
'1' == 1; // type coercion occurs
// => true 
'1' === 1; 
// => false
```

Here are some examples of calling String object properties, on a primitive string:

```javascript
// some examples of String properties: 
const someString = "Lighthouse Labs"; 

console.log(someString.toUpperCase()); 
// => 'LIGHTHOUSE LABS'

console.log(someString.toLowerCase()); 
// => 'lighthouse labs'

console.log(someString.split("")); 
// => [ 'L', 'i', 'g', 'h', 't', 'h', 'o', 'u', 's', 'e', ' ', 'L', 'a', 'b', 's' ]
```

If you'd like another source to read more about JavaScript values, please continue onto this reading [here](https://2ality.com/2011/03/javascript-values-not-everything-is.html)


