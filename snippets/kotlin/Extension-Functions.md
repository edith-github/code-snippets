## WRITING EXTENSION FUNCTIONS IN KOTLIN:

Two String [extension functions](https://kotlinlang.org/docs/reference/extensions.html) to demonstrate how to count the words in a String.

```kotlin

fun String.wordCount(): Int {
    if (this.isBlank()) {
        return 0
    }
    return this.split(" ").filter { it.isWord() }.size
}

fun String.isWord(): Boolean {
    val filter = this.filter { it in 'A'..'Z' || it in 'a'..'z' }
    return !filter.isBlank()
}

/**
 * Usage example
 */
fun main(args: Array<String>) {
    var testString = "String."
    println(testString.wordCount())//1

    testString = "One two three"
    println(testString.wordCount())//3

    testString = " one two    three four"
    println(testString.wordCount())//4

    testString = " one tow    three four! five"
    println(testString.wordCount())//5

    testString = " !! !    . ..!"
    println(testString.wordCount())//0
}
```

0
0
4
4
8
