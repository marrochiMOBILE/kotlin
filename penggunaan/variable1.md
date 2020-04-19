# variable 

ada dua variable didalam kotlin yaitu `var` dan `val` . perbedaanya jika var adalah nilai yg bisa diubah sedangkan val nilainya tetap kalo di php seperti `define` kalo di javascript `const`. 

> disisni variabel tanpa penegasan jadi bisa berupa nilai apa ajja
```kotlin
var teks1 =  "nilai tanpa penegesan"
var teks1b = 20

println("teks1: $teks1 teks1b : $teks1b")
```

> coba bandingkan dengan variabel penegasan
```kotlin
val nama:String = "marrochi"
val pi:Float = 3.14f
val nilai:Int = 10
val db:Double = 218872.1292112
```
jika penegasan seperti ini itu harus sesuai dengan penegasanya jika `val nama:String = 10` itu akan terjadi error
