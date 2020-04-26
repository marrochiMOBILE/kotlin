# functions 1

### tanpa parameter
lihat contoh dibawah ini :
```kt
fun  tampilkan1(){
        println("ini adalah tampilan satu")
}

fun main(){
        tampilkan1() // memanggil function
        tampilkan2() // memanggil function
}

fun tampilkan2(){
        println("ini adalah tampilan 2")
}
```
output:
```
ini adalah tampilan satu
ini adalah tampilan 2

```

### menggunakan parameter

Fungsi memiliki dua parameter Int dengan tipe pengembalian Int:

```kt
fun sum(a: Int, b: Int): Int {
        return a + b
}

fun main() {
        print("sum of 3 and 5 is  = ")
        println(sum(3, 5))
}
```

output :
```
sum of 3 and 5 is  = 8
```


Berfungsi dengan tubuh ekspresi dan tipe pengembalian yang disimpulkan:
```kt
fun sum(a: Int, b: Int) = a + b

fun main() {
        println("sum of 19 and 23 is ${sum(19, 23)}")
}
```
output :
```
Fungsi tidak mengembalikan nilai yang berarti:
```kt
fun printSum(a: Int, b: Int): Unit {
        println("sum of $a and $b is ${a + b}")
}

fun main() {
        printSum(-1, 8)
}
```
output:
```
sum of -1 and 8 is 7
```


Jenis pengembalian unit dapat dihilangkan:
```kt
fun printSum(a: Int, b: Int) {
        println("sum of $a and $b is ${a + b}")
}

fun main() {
        printSum(-1, 8)
}
```
output:
```
sum of -1 and 8 is 7
```
