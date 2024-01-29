
# 5 Similarities between Kotlin and TypeScript

Recently I started working with Kotlin. I couldn't help but wonder how syntax was similar to TypeScript language. In this blog post, I want to provide 5 similaries I found in these languages with examples.


## 1. Variable Type declarations
While declaring variables, we can mention type of the variable in both the languages.


### Kotlin
```Kotlin
val helloWorldString: String = "Hello World!"
```

### TypeScript
```TypeScript
const helloWorldString: String = 'Hello World!';
```

## 2. Function declarations with default values
In both languages, we can declare default values for parameters in function along with types. This comes in handy while dealing with cases where the parameter is not passed in while invoking function and need to check the type of data passed to the function.

### Kotlin
```kotlin

fun greetHi(name: String, greeting: String = "Hello") {
    println("${greeting}! ${name}")
}

greetHi("Lalitha", "Hi"); // Prints "Hi! Lalitha"
greetHi("Lalitha");  // Prints "Hello Lalitha"

```

### TypeScript

```TypeScript
function greetHi(name: String, greeting: String = 'Hello') {
    console.log(`${greeting}! ${name}`);
}
greetHi('Lalitha', 'Hi'); // Prints "Hi! Lalitha"
greetHi('Lalitha');  // Prints "Hello Lalitha"
```

## 3. Lambda expressions
Lambda functions are a convenient way of declaring functions. It makes it easier to pass functions as parameters to other functions.

### Kotlin

```Kotlin
val greetHi: (String, String) -> String  =  { name, greeting ->  "${greeting}! ${name}"}

println(greetHi("Lalitha", "Hi")) // Prints "Hi! Lalitha"

```


### TypeScript
TypeScript offers fat arrow functions similar to lambda functions in Kotlin.
```typescript
let greetHi: (name:String, greeting:String) => String = function (name, greeting){ return `${greeting}! ${name}`;}

console.log(greetHi("Lalitha", "Hello")); // Prints "Hello! Lalitha"

```

## 4. Nullable values
Both Kotlin and TypeScript provide a way to declare null or undefined variable or function parameter. Having nullable variable comes in handy to avoid errors when trying to access parameter of nullable variable.

### Kotlin
```kotlin
var maybeHelloStr: String? = null
printHelloWorld(maybeHelloStr)

fun printHelloWorld(maybeHelloStr: String?) {
  println("Hello string: ${maybeHelloStr}")
}
```


### TypeScript
```typescript
let maybeHelloStr?: String = undefined

printHelloWorld(maybeHelloStr)

function printHelloWorld(maybeHelloStr?: String) {
  console.log(`hello string: ${maybeHelloStr}`);
}
```

## 5. Generic type
Both Kotlin and TypeScript provide a generic type any.

### Kotlin
```Kotlin
var anyValue: Any
anyValue = "hello"

println(anyValue) // Prints "hello"

anyValue = 5
println(anyValue) // Prints 5

```


### TypeScript

```TypeScript
let anyValue: any
anyValue = "Hello"

console.log(anyValue) // Prints "Hello"
anyValue = 5
console.log(anyValue) // Prints 5

```

Please try out Kotlin online [playground](https://play.kotlinlang.org/) and TypeScript [playground](https://www.typescriptlang.org/play) to run the code snippets to explore further.

See you in my next blog post!
