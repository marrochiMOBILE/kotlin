# variable

**[** TEMPAT BELAJAR **]** 
https://kotlinlang.org/docs/tutorials/kotlin-for-py/declaring-variables.html

ada dua variable di kotlin yaitu **`var`** dan **`val`**

1. **var** bisa dibilang var ini nilainya bisa diubah
1. **val** nilainya tidak bisa diubah

yuk langsung kuy aja 

```kotlin
var INIstring =  "ochi" // catatan untuk string menggunkan kutip dua "value"
var INIinteger = 10
var INIfloat = 165.0f
var INIdouble = 33.0
```
anda jugha bisa menggunkan penegesan untuk nilainya dengan menggunakan tanda **`:`** titik dua.

```kotlin
    var INIinteger:Int = 10
    var INIdouble:Double = 33.0
    var INIfloat:Float = 165.0f
    var INIstring:String = "ochi"
```


## Declaring variables

Setiap variabel harus dideklarasikan. Upaya apa pun untuk menggunakan variabel yang belum dideklarasikan adalah kesalahan sintaksis; dengan demikian, Anda dilindungi dari penetapan tak sengaja ke variabel yang salah eja. Deklarasi ini juga memutuskan jenis data apa yang Anda boleh simpan dalam variabel.

Variabel lokal biasanya dideklarasikan dan diinisialisasi pada saat yang sama, dalam hal ini jenis variabel disimpulkan sebagai jenis ekspresi yang Anda inisialisasi dengan:

```kt
var number = 42 // integer
var message = "Hello" // string [ingat harus pake kutip " "]
```

coba tambahkan terus jalankan
```kt
number = 10
number += 7
println(number) // 17
println(message + " there") // Hello there
```


## Read-only variables
Variabel lokal read-only didefinisikan menggunakan val kata kunci. Mereka dapat diberi nilai hanya sekali.
```kt
val a: Int = 1  // immediate assignment
val b = 2   // `Int` type is inferred
val c: Int?  // Type required when no initializer is provided
c = 3       // deferred assignment
println("a = $a, b = $b, c = $c")
```

## Variables that can be reassigned
```kt
fun main() {
        var x = 5 // `Int` type is inferred
        x += 1
        println("x = $x") // 6
}
```

## terakhir
```kt
// variabel global
val PI:Double = 3.14
var x:Int = 0

fun incrementX() {
        x += 1
}

fun main() {
        println("x = $x; PI = $PI")
        incrementX()
        println("incrementX()")
        println("x = $x; PI = $PI")
}
```
