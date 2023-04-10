
Typescript knows the [[JavaScript]] language and will generate default types for you

Some design patterns (e.g. [[dynamic programming]] ) make it difficult for types to be automatically inferred.

TS supports extension of JS where you can inform TS what your types should be

``` typescript
interface User {  name: string;  id: number;}
```

``` typescript
const user: User = {  name: "Hayes",  id: 0,};
```

TS will warn if object doesn't match interface provided. 

Classes + OO programming: 

``` typescript
interface User {
	name: string;  id: number;
	} 
	
class UserAccount {
	name: string;  
	id: number;   
	
	constructor(name: string, id: number) 
		{this.name = name;    this.id = id;  }}
		
const user: User = new UserAccount("Murphy", 1);
```

Use interfaces to annotate params + return values 

Primitive types that can be used in interfaces:

`boolean`, `bigint`, `null`, `number`, `string`, `symbol`, and `undefined`

Typescript extends with: `any`, `unknown` (type must be declared by implementer), `never` (not possible for type), `void` (returns `undefined` or has no return value).

Prefer `interfaces` over `type`s unless you need its specific features.

Composing types - create complex types by combining simple ones. Do via uninons or generics. 

### Unions  

Use `|` operator , often used to describe a set of types that a value is allowed to be 

``` typescript
type WindowStates = "open" | "closed" | "minimized";type LockStates = "locked" | "unlocked";type PositiveOddNumbersUnderTen = 1 | 3 | 5 | 7 | 9;
```
Also used for handling different types: 

``` typescript
function getLength(obj: string | string[]) {  return obj.length;}
```
Use `typeof` to learn type:

|    Type   |             Predicate            |
|:---------:|:--------------------------------:|
| string    | typeof s === "string"            |
| number    | typeof n === "number"            |
| boolean   | typeof b === "boolean"           |
| undefined | typeof undefined === "undefined" |
| function  | typeof f === "function"          |
| array     | Array.isArray(a)                 |

``` typescript
type StringArray = Array<string>;  
type NumberArray = Array<number>;  
type ObjectWithNameArray = Array<{ name: string }>;   
```

### Duck typing

TS checks the shape that values have - if an object is declared using the shape of a known interface it will 


Sources:
https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html
