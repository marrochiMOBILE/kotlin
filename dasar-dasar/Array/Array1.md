# Array 1
array adalah kumpulan data-data karena jika ditampung dengan variabel biasa sangat menghambur variabel tersebut
```kt
    var nilai2 = Array<Int>(5){0}
    nilai2[0] = 88
    nilai2[4] = 69
    println("mencetak array ke [0]  :   ${nilai2[0]}")
    println("mencetak array ke [5]  :   " + nilai2[4])


  // menampilkan semua array
    println()
    for (for2 in nilai2){
        println(for2)
    }
```

output:
```
88
0
0
0
69
```

#### contoh dijelaskan 
var nilai2 = Array<"1">("2"){"3"}

1. disini berupa tipe datanya ke integer atau yg lain
1. besarnya array misal diisi 5 berarti array tersebut 0,1,2,3,4 bila ditotal 5
1. terus disini value untuk array yg belom diisi 


## menggunakan readLine
```kt
 var nilai3 = Array<String>(5){""}
    for(for3 in 0..4){
        print("masukan nama nama anda : ")
        nilai3[for3] = readLine()!!
    }

    println("nilai ke 2 : "+nilai3[2])
```



