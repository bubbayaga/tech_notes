100% interop with Java. 

Only mentioning notable changes as I know Java already. 

### Entrypoint

``` kotlin
fun main(args: Array<String>) { 
	// do  stuff
	}
```

Since 1.3 can be defined without any params

## Variables

`val` = cannot be reassigned
`var` = can be reassigned 

## Types

Kotlin can usually determine types automatically, define explicitly via:

``` kotlin
val foo: Int = 7
```

## Strings

Rawstring uses `"""`

Support template expression, starts with dollar sign. 

### Null

For a var to validly hold null must be explicitly specified as nullable. Specify by using `?` operator, access by using `?.`  and `?:` to specify alternate value

``` kotlin
var fooNullable: String? = "abc"
    println(fooNullable?.length) // => 3
    println(fooNullable?.length ?: -1) // => 3
    fooNullable = null
    println(fooNullable?.length) // => null
    println(fooNullable?.length ?: -1) // => -1
```


## Functions

``` kotlin
fun hello(name: String = "world"): String {
        return "Hello, $name!"
    }
```

`vararg` keyword allows variable number of args to be passed

 When a function consists of a single expression then the curly brackets can be omitted. The body is specified after the = symbol.

    fun odd(x: Int): Boolean = x % 2 == 1

If return type can be inferred then no need to specify it. 

Functions can take funcs as argument and return functions

``` kotlin
fun not(f: (Int) -> Boolean): (Int) -> Boolean {
        return {n -> !f.invoke(n)}
    }
```

Named functions can be used as args using `::` operator

e.g.
`val notOdd = not(::odd)`

Can use lambda expressions as arguments. If lambda only has one argument then declaration (with the `->` can be omitted). The name of the single arg will always be `it`

## Classes

Declare via `class` keywork

New instances are created using contructor, there is no 'new' operator. 

Member functions can be called using dot notation. 

If function is marked with `infix` keyword then it can use [[infix notation]]

#### Data

Concise way of creating classes that just hold dath. Hashcode / equals and `toString` methods are automatically generated. 

Data classes have a `copy()` function where you can replace some of the values via method args

can desctruct objects into multiple variables

``` kotlin
val (a, b, c) = DataClassExample(1,2,4)
println("$a, $b, $c") // 1,2, 4
```

Can also destruct in a forloop

``` kotlin
for ((a, b, c) in listOf(fooData)) {
        println("$a $b $c") // => 1 2 4
    }
```


Has a `with()` function, lets you mutate a mutable data class

## Lists

Declare using `listOf()` - immutable

access by index

mutableLists can be created using `mutableListOf`





https://learnxinyminutes.com/docs/kotlin/

