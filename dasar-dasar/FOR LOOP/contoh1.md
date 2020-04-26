# for
perulangan menggunakan for
### 1.1 for in
```kt
    for(cetak in 1..3){
        println("ini adalah cetakan : $cetak")
    }
```
output:
```
ini adalah cetakan : 1
ini adalah cetakan : 2
ini adalah cetakan : 3
```
### 1.2 for in
```kt
        for(cetak in 1..100){
            if(cetak == 99){
                println("anda berada di posisi $cetak")
            }
        }
    print("pengulangan selesai")
```
output:
```
anda berada di posisi 99
pengulangan selesai
```

### 1.3 for in
```kt
fun main() {
    val items = listOf("apple", "banana", "kiwifruit")
    for (item in items) {
        println(item)
    }
}
```

output:
```
apple
banana
kiwifruit
```

## indices
```kt
 val items = listOf("apple", "banana", "kiwifruit")
    for (index in items.indices) {
        println("item at $index is ${items[index]}")
    }
```

output:
```
item at 0 is apple
item at 1 is banana
item at 2 is kiwifruit
```

