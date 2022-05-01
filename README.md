# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

////NoTES

// let name: string;
// let age: number;
// let isStudent: boolean;
// let hobbies: string[]; // or number[]  is the same as Array<number>.. T<U>sytnax is for covering generics
// let role: [number, string]; //tuple is anything INSIDE the brackets

//let printName: Function;  // there is a better way to define the type of a function
//let printName: (name: string) => void; // this is a good way to define the return type (where void is)
//let printName: (name: string) => number;  // however typescript will otherwise infer a type for a return based on the return statement
// fucntion printName(): string { return "Phil" } // this is another way to define the type of the returna string 

// let obj: any = { x: 0} // this prevent any type being defined for obj (allows all types// no typing// turns offf type for that variable).

// compile with noImplicitAny  to prevent types being defined defult any  // this usually will implicit any


// //implicitany vs inferredReturn/contextualTyping -

//typescriptlang.org/docs/handbook/intro.html

//In modern JavaScript a property can be checked in the call of a method:  obj.last?.toUpperCase()
//Union Types
// Typescripts type stytsm allow s you to build  enew types ot o f exising one
// any of this or that type   `|`
// by default "|" requires that the operations wtih this type work for both sides of the union
// Using Narrowing.  Narrowing occurs withen you use conditionals to filter out each type and give different isntructions for each type.
//let printName: (name: string) => never;

// type never is a tool for actions that are meant to never produce a value // (storage for ) // internal intaeractions
   // never is something that cannot return// it alwasy throws
   // opeing and closing files, switch functions with an exhaustive check for cases, 


//type unknown requires a type definition before it can be applied (no implicit) // type assertion can resolve the unknown type to a specific type



//here is a 'type alias '
//  // type Point = {
    //   x: number;
    //   y: number;
    // }
// Point is the type alias
// Here's another one:  // type ID = number | string // ID is an alias that represents a union type definition

// 

// Yyou can dd new fields to the interface Window
// interface Window {
//   title: string
// }
// interface Window {
//   ts: TypeScriptAPI 
// }
//const src = 'const a = "hellow world"';
//window.ts.transpileModule(src, {});

// You cannot do that with Types.  type Window = {...} is the creation of a type as a constant object // so type Window  = //repeated is trying to assign a new value to a constant

//Type Assertions 
// Type assertions is at the end of the declaration or definiition there is a phrase "as TypeNameExample"
//  Ex:  const x = "hello" as string //or// const array1 = [] as number[] // for changing specificity



//UNION
// a union of string literals "left" | "right" | "center" has value as a data validation tool

// a union of Numeric Literals -1| 0 | 1 is a union of constants that can be used as to validate the output of a function.

//Literal Inferance
// TypeScript implicitly assumes the type to be the data type and not the literal type 
// therefore if it is possible that the argument of a function may be of an invalid type, use a type assertion as a literal to clarify that you expect a specific acceptible value 

//strictNullChecks OFF
// // TypeScript Types "null" and "undefined" behave depending on the strictNullChecks option.  Without strictNullChecks they can be assigned to aproerty of any type.
 // // This is where a lot of bugs from C# and Java come from!  So try out strictNullChecks if it is practical

 //strictNullChecks ON  
  // // you need to test for those values before using methods or properties on that value.  Just like checking for undefined before using an optional propertiy -- use Narrowing\
  // // // 
  // function doSomething(x: string | null) {
  //     if (x === null) {
  //           //do nothing
  //     } else {
  //       console.log("hello, " + x.toUpperCase());
  //     }
  // }

// x!.methodExample()   the ! prevents types null and undefined  /// a type assertion that the vaule is NOT null or unefined // 
//  // // Non-null Assurtion Operator(Postfix !) only use (!) it if YOU KNOW it CANNOT be null or undefined



// // interface declaration 
// interface Point {
//   x: number;
//   y: number;
// }
 



// Type is an ALIAS
// the other ALIAS is an Interface
// 

// BOth aliases can be applied in exactly the same way on an instance
// but an interface can be changed and recombined, however a Type has to be chained into a new TYPE //// a type is constant


// interface Person { 
//    name: string;
//    age?: number;
// };

// type X = {
//   a: string;
//   b: number;
// };
//what if we want to use peroprties of type X in type Y?
// type Y = X & {
//   c: string;
//   d: number;
// }

// let y: Y = {
//   c: 'efdas',
//   d: 43,
  
// };  // this would break because it MUST have the properties defined in Type X

// Use Interface a LOT unless you know EXACTLy what you should be expecting 


// type W = Person & {
//   e: number;
//   f: string;
// }

// interface Gal extends W {
//   profession: string;
// }
// 


// function printName(name: string) {
//   console.log(name);
// }

// function App() {
//   return (
//     <div className="App">
//     </div>
//   );
// }