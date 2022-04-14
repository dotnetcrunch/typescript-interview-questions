# TypeScript Interview Questions and Answers

<blockquote>Click ⭐️ if you like the content. Pull Request are highly appreciated.</blockquote>

Follow [dotnetcrunch](https://github.com/dotnetcrunch) for more.

### 01. What is TypeScript?
TypeScript is an open-source object-oriented programming language developed and maintained by Microsoft. It is a superset of JavaScript.

TypeScript is designed for the development of large applications and transpiles to JavaScript.

### 02. Why do we need TypeScript?
TypeScript is an attempt to fix JavaScript problems.

Since we all know that JavaScript is the only language used in client-side scripting as browsers can only understand JavaScript.

Since TypeScript simplifies JavaScript code, making it easier to read and debug. It saves developers time and increases productivity.

### 03. What are the benefits of using TypeScript?
Benefits of using TypeScript:

- Integrates well with React, Vue, and Angular.
- Is a statically typed language and this makes the code easier to refactor. 
- Is easier to read and access. Helps in code maintainability.
- Has a powerful type system, including generics.
- Gives all the benefits of ECMAScript 6, thus improves productivity.
- Statically typed programming languages are those in which the type of a variable is known at compile-time instead of at run-time.

### 04. How to install TypeScript?
There are two ways to install typescript:

Using npm (Node Package Manager)
Install the TypeScript plugin in your IDE
```ts

> npm install -g typescript

```

You can also install a typescript plugin available for your IDE. You can use IDE of your choices such as VS Code, Visual Studio, Atom, or Sublime Text.

### 05. Explain the TypeScript program execution?
TypeScript totally follows the OOPS (Object-Oriented Programming System) concept and with the help of TSC (TypeScript Compiler), we can convert Typescript code (.ts file) to JavaScript (.js file).


### 06. What OOPs does TypeScript support?
Typescript supports the four pillars of any object-oriented programming language that are – Abstraction, Polymorphism, Inheritance, and Encapsulation.

### 07. Explain data types in TypeScript?
Typescript supports Any, Built-in, and User-defined data types.

Any is the superset for all the data types available. It means that the variable could be of any type. It will override the type checking.

The Built-in types include string, number, boolean, undefined, null, and void.

The User-defined types include array, enum, interface, class, union, and tuple.

### 08. What are the modules in TypeScript?
A module is a way to construct a local scope in a file. So that all the classes, variables declared in a module are not accessible outside the module.

We can create a module using the export keyword.
A module in typescript can be used in another module using the import keyword.

### 09. What is a namespace in TypeScript?
Using namespace we can group logically related code. This is built into typescript, unlike javascript. A namespace can include classes, interfaces, functions, and variables.

We can create a namespace in typescript using namespace keyword followed by any valid name.

For Example:

```ts

namespace MyNamespace {

}
```

### 10. What are typed functions in TypeScript?
In Typescript, a function can be created as a named function or anonymous function. We can further add types to each of the parameters and to the function as well.

```ts

// Named function
function add(a: number, b: number) : number {
    return a + b;
}

// Anonymous function
let funcAdd = function(a: number, b: number): number { return a + b; };
```

If we want to write the full type of the function:

```ts

let funcAdd: (a: number, b: number) => number = 
     function (a: number, b: number) : number  { return a + b; };
```
     
### 11. What is as syntax in TypeScript?
This is an additional Type assertion syntax. The reason for including the as syntax in typescript was that <type> conflicted with JSX.

```ts

let strLength: number= (someString as string).length;
```

### 12. Difference between readonly and const?
The difference between readonly and const is: const is used on a variable whereas read-only is used on properties of an object.

### 13. What are static properties?
Static properties are those that are shared by all the instances of a class and they can be accessed via the class name and dot operator.

```ts

class Singleton {
    static counter = 0;
    constructor() {
        Singleton.counter++;
    }
  }
  
  var singleton = new Singleton();
  console.log(Singleton.counter); //1
```  
  
### 14. Explain access modifiers in Typescript?
There are 3 types of access modifiers in TypeScript: public, private, and protected.

#### Public

By default, all the members of a class are public in TypeScript.

#### Private

When any of the class members are declared private, it is only accessible within the class scope.

#### Protected

The protected members are similar to private access modifiers, except that they are accessible in the derived class.

### 15. Can you explain Rest parameters in Typescript?
Sometimes, we want to work with multiple parameters as a group, or we may not know how many parameters a function will ultimately take. In JavaScript, we have something known as arguments. Similarly, we have Rest parameters in typescript.

Rest parameters are treated as a boundless number of optional parameters. The compiler will build an array of the arguments passed in with the name given after the ellipsis (…)

```ts

function getPlayersList(name:string, ...players: string[]) {
    return name + " " + players.join(" ");
}

let players = getPlayersList("Virat", "MS", "Warner", "Kane", "Ben")
```

### 16. What are Generics in TypeScript?
Generics in Typescript is no different than generics in other programming languages like C# or Java.

You can create a class, an interface, or a function that works with different types, without specifying the type upfront.

```ts

function greet(a : T) {
  console.log(`Hi ${a}!`)
}

greet('DS'); //function call

```

The symbol T identifies a generic type.

### 17. What is Modules in TypeScript?
A module is a way to construct a local scope in a file. So that all the classes, variables declared in a module are not accessible outside the module.

👉 We can create a module using the export keyword.
👉 A module in typescript can be used in another module using the import keyword.

```ts

export class Student {
    readonly Id: number;
    Name: string;
    
    constructor(id: number, name: string) {
        this.Id = id;
        this.Name = name;
    }
}

let Subject: string = "Computer Science";
```

### 18. Can we use JSX in TypeScript?
Yes, JSX is an embeddable XML-like syntax.

In order to use JSX, we must name our file with a .tsx extension and should enable jsx option.

### 19. What are Decorators in TypeScript?
Decorators are functions that modify a class, property, method, or method parameter. The syntax to define decorators is “@”.

In other words, Decorators are functions that take their target as the argument.

### 20. What is Triple-Slash Directive?
Triple-slash directives are single-line comments containing a single XML tag. The contents of the comments are used as compiler directives.

```ts

 /// <reference path = "filename.ts" />
 ```
Triple-slash directives are only valid at the top of their containing file.

### 21. What is the ts.config file in Typescript?
The typescript project will have a ts.config file which provides an infinite number of ways to customize the behavior of the compiler.
typescript interview questions

### 22. Is it possible to compile a typescript file automatically?
Yes, it is possible using --watch option while compiling the typescript file for the first time.

```ts

tsc --watch filename.ts
```

### 23. Explain the Declare keyword in Typescript?
The declare keyword is used for ambient declarations and methods where you want to define a variable that may exist elsewhere.

If we want to use any library in our TypeScript code, we can use the following code:

```ts

declare var myAlexaLibrary;
```

### 24. Explain the need for a TypeScript Definition Manager?
TypeScript Definition Manager (TSD) is a package manager used to search and install typescript definition files directly from the community-driven DefinitelyTyped repository.

Now, if you want to use some jQuery code in your .ts file:

```ts

$(document).ready(function() { //Your jQuery code });
```

Here, when you try to compile it by using tsc, it will give a compile-time error: Cannot find the name “$”.

So, you need to inform the TypeScript compiler that “$” is belongs to jQuery.

To do this, TSD comes into play. You can download the jQuery Type Definition file and include it in our .ts file.

### 25. How to debug a TypeScript file?
To debug any TypeScript file, we need a .js source map file. So, we have to compile the .ts file with the --sourcemap flag to generate a source map file.

```ts

$ tsc -sourcemap filename.ts
```

This will create a filename.js and filename.js.map. And the last line of filename.js would be a reference to the source map file.

```ts

//# sourceMappingURL=filename.js.map
```

### Closing Notes
We hope that you like the above-listed TypeScript interview questions.

All the best for your preparation 😊

You can also share this list of typescript interview questions and answers with your friends with the help of the below-sharing options.

### Bonus Content
In case you are interested in a step by step typescript tutorial then navigate to our tutorial space:

👉 [TypeScript Tutorial](https://tutorialsnest.com/typescript-get-started/) 
