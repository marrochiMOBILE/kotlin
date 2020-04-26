# function 2

### Conditional expressions
```kt
fun maxOf(a: Int, b: Int): Int {
    if (a > b) {
        return a
    } else {
        return b
    }
}

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}") // max of 0 and 42 is 42
}
```

tapi jika didalam kotlin anda bisa menggunakan expression berikut:
```kt
fun maxOf(a: Int, b: Int) = if (a > b) a else b

fun main() {
    println("max of 0 and 42 is ${maxOf(0, 42)}") // max of 0 and 42 is 42
}
```

## Nullable values and null checks / Nilai tidak dapat dibatalkan dan cek nol

Referensi harus secara eksplisit ditandai sebagai nullable ketika nilai nol dimungkinkan.

Kembalikan nol jika str tidak memiliki bilangan bulat:

```kt
fun parseInt(str: String): Int? {
    // ...code...
}
```

Gunakan fungsi yang mengembalikan nilai nullable:
```kt
fun parseInt(str: String): Int? {
    return str.toIntOrNull()
}

fun printProduct(arg1: String, arg2: String) {
    val x = parseInt(arg1)
    val y = parseInt(arg2)

    // Using `x * y` yields error because they may hold nulls.
    if (x != null && y != null) {
        // x and y are automatically cast to non-nullable after null check
        println(x * y)
    }
    else {
        println("'$arg1' or '$arg2' is not a number")
    }    
}


fun main() {
    printProduct("6", "7")
    printProduct("a", "7")
    printProduct("a", "b")
}
```

output:
```
42
'a' or '7' is not a number
'a' or 'b' is not a number
```
toIntOrNull() adalah sebuah method yg mengembalikan nilai integer kalo g null

```kt
fun parseInt(str: String): Int? {
    return str.toIntOrNull()
}

fun printProduct(arg1: String, arg2: String) {
    val x = parseInt(arg1)
    val y = parseInt(arg2)
    
    // ...
    if (x == null) {
        println("Wrong number format in arg1: '$arg1'")
        return
    }
    if (y == null) {
        println("Wrong number format in arg2: '$arg2'")
        return
    }

    // x and y are automatically cast to non-nullable after null check
    println(x * y)
}

fun main() {
    printProduct("6", "7")
    printProduct("a", "7")
    printProduct("99", "b")
}
```

output:
```
42
Wrong number format in arg1: 'a'
Wrong number format in arg2: 'b'
```
 ## Type checks and automatic casts
 Operator is memeriksa apakah ekspresi adalah turunan dari tipe. Jika variabel atau properti lokal yang tidak dapat diubah diperiksa untuk jenis tertentu, Anda tidak perlu mengubahnya secara eksplisit:
 
 ```kt
 fun getStringLength(obj: Any): Int? {
    if (obj is String) {
        // `obj` is automatically cast to `String` in this branch
        return obj.length
    }

    // `obj` is still of type `Any` outside of the type-checked branch
    return null
}


fun main() {
    fun printLength(obj: Any) {
        println("'$obj' string length is ${getStringLength(obj) ?: "... err, not a string"} ")
    }
    printLength("Incomprehensibilities")
    printLength(1000)
    printLength(listOf(Any()))
}
 ```
 
 or
 ```kt
 fun getStringLength(obj: Any): Int? {
    if (obj !is String) return null

    // `obj` is automatically cast to `String` in this branch
    return obj.length
}


fun main() {
    fun printLength(obj: Any) {
        println("'$obj' string length is ${getStringLength(obj) ?: "... err, not a string"} ")
    }
    printLength("Incomprehensibilities")
    printLength(1000)
    printLength(listOf(Any()))
}
 ```
 
 output
 ```
 'Incomprehensibilities' string length is 21 
'1000' string length is ... err, not a string 
'[java.lang.Object@3af49f1c]' string length is ... err, not a string 
 ```
 
 atau menggunakan even
 ```kt
 fun getStringLength(obj: Any): Int? {
    // `obj` is automatically cast to `String` on the right-hand side of `&&`
    if (obj is String && obj.length > 0) {
        return obj.length
    }

    return null
}


fun main() {
    fun printLength(obj: Any) {
        println("'$obj' string length is ${getStringLength(obj) ?: "... err, is empty or not a string at all"} ")
    }
    printLength("Incomprehensibilities")
    printLength("")
    printLength(1000)
}
 ```
 output :
 ```
 'Incomprehensibilities' string length is 21 
'' string length is ... err, is empty or not a string at all 
'1000' string length is ... err, is empty or not a string at all 
 ```
 



