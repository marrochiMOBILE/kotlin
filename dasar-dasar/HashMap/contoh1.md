# HashMap 
Map dan HashMap merupakan data Collection yang digunakan untuk menyimpan data dengan jumlah yang banyak, seperti Array. 

```kt
 var nilai = HashMap<Int, String>()
    nilai.put(1, "Ibrohim")
    nilai.put(2, "john")
    nilai.put(3, "alexsandro")
    nilai.put(42, "lala")
    println("nama yg tampil adalah ${nilai.get(2)}")
//    di update
    nilai.put(3, "alexsandro wijoyo")

//    loop menampilkan semua
    for(k in nilai.keys){
        println(nilai.get(k))
    }
```

output :
```kt
nama yg tampil adalah john
Ibrohim
john
alexsandro wijoyo
lala
```
