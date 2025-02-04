## Kotlin
- No use use of semicolon
```kotlin
fun main() {
    println("saif")
}
```

- Variable Declaration
```kotlin
fun main() {
	val count: Int = 2
	println(count)
}
```

- Type Inference => Kotlin compiler will detect the data type if you do not give any value after colon but if you do not initialize a value you have to give the datatype as well.
```kotlin
fun main() {
	val count = 2
	val nocount: Int
}
```

- Basic math operations
```kotlin
fun main() {
	val count = 3
	val noCount = 4
	println("Sum of the two are ${count + noCount}")
}
```

- user `var` when you have to change the value of a variable and `val` when you want a constant value or fixed value for a variable.

- Refer to [kotlin style guide](https://developer.android.com/kotlin/style-guide)

- Increment and Decrement operators
```kotlin
fun main() {
	var count = 2
	var noCount = 3
	count += 1
	println(count)
	noCount -= 1
	println(noCount)
}
```

```kotlin
fun main() {
	var count = 2
	var noCount = 4
	count++
	noCount--
	println("Total: ${count + noCount}")
	println("Total: ${count - noCount}")
}
```

- Other Data Types
```Kotlin
fun main() {
	var count: Double = 2.0
	// var count: Double = 2 // mismatch kotlin.Int
	val trip1 = 4.5
	val trip2 = 5.6
	val trip = trip1 + trip2
	println(trip)
	// for float add f or F
	val trip3 = 3.4f // or 3.4F
}
```

```kotlin
fun main() {
	val name: String = "saif"
	val firstLetter: Char = 's' // single quotes for char and double for string	
}
```

- Escape Sequence
	-  `\t` – tab
    
	- `\b` – backspace
    
	- `\n` – new line (LF)
    
	- `\r` – carriage return (CR)
    
	- `\'` – single quotation mark
    
	- `\"` – double quotation mark
    
	- `\\` – backslash
    
	- `\$` – dollar sign

```kotlin
fun main() {
	val disable: Boolean = false;
	val enable: Boolean = true;
	println("Disable or Enable: " + disable)
}
```

You can concatenate other data types to strings just use `+`

- Coding Conventions
	-  Variable names should be in camel case and start with a lowercase letter.
	
	- In a variable declaration, there should be a space after a colon when you specify the data type.
	
	- There should be a space before and after an operator like the assignment (`=`), addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`) operators and more.
	
	- As you write more complex programs, there is a recommended limit of [100 characters per line](https://developer.android.com/kotlin/style-guide#line_wrapping). That ensures that you can read all the code in a program easily on your computer screen, without needing to scroll horizontally when reading code.

- Functions
```kotlin
fun main() {
	// entry point for program
	println("name") // funciton
}
```

```Kotlin
fun main() {
	birthdayGreeting()
}

fun birthdayGreeting(): Unit {
	println("Happy Birthday")
}
```

In Kotlin we have Unit equivalent to void in java when a function does not returns any value

Returning a string
```kotlin
fun main() {
	val greetings = birthdayGreeting()
	println(greetings) // println(birthdayGreeting())
}

fun birthdayGreeting(): String {
	val greet = "Happy Birthday"
	return greet
}
```

Add a parameter to function `birthdayGreeting()`
```kotlin
fun main() {
	val greetings = birthdayGreeting("saif")
	println(greetings) // println(birthdayGreeting())
}

fun birthdayGreeting(name: String): String {
	val greet = "Happy Birthday $name"
	return greet
}
```
parameters in kotlin are immutable