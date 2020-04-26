# string 1
ingat string harus menggunakan kutip dua  **`" "`**;
```kt
var kalimat = "iNi adGlah kaLimat"

//    mencetak semuanya
println(kalimat) // iNi adGlah kaLimat
```

mencetak sebagian  yg dihitungnya dimulai dari nol
```kt
 println(kalimat[4]) // a
```

## length
menceteak jumlah charakter yg dihitungnya dimulai dari satu
```kt
println(kalimat.length) // 18
```

## toUpperCase
merubah jadi huruf besar semua
```kt
println(kalimat.toUpperCase()) // INI ADGLAH KALIMAT
```

##  toLowerCase
merubah huruf jadi kecil semua
```kt
  println(kalimat.toLowerCase()) //  ini adglah kalimat
```
## split
pemecah string dan merubahnya dalam bentuk array 
```kt
 println(kalimat.split(" ")) // [iNi, adGlah, kaLimat]
```

## trim
memotong space yg kosong dibagian awal dan akhir
```kt
var xx =  " o k "
println(xx.trim().length) // 3
println(xx.length) // 5
```

## replace
mengganti string lama ke string yg baru
```kt
fun main() {
        var a = 1
        // simple name in template:
        val s1 = "a is $a"

        a = 2
        // arbitrary expression in template:
        val s2 = "${s1.replace("is", "was")}, but now is $a"
        println(s2)
}
```

output:
```
a was 1, but now is 2
```

