# ekpresi if dan when

### 1.1 if else
```kt 
 var nilai1:String?
    print("masukan nilai 0 - 10  :")
    nilai1 = readLine()!!.trim()
    if(nilai1.toInt() > 10 ){  // jika kondisinya lebih dari 10 maka block didalam akan dieksekusi
        println("angka yg anda masukan di atas 10")
    }
    else{ // ketika kondisi semua salah maka kondisi ini yg akan dijalankan
        println("angka yg anda masukan dibawah 10")
    }
```
### 1.2 if else
if dan else ditaruh kedalam variabel dalam baris yg sama
```kt
    print("masukan angka nilai 0 - 10 :  ")
    var nilai:Int = readLine()!!.toInt()
    var cetak:String = if(nilai > 10) "nilai anda lebih dari 10" else "nilai anda kurang dari 10"
    print(cetak)
```

### 1.3 When
hampir sama dengan if cuman ada perbedaan silahkan anda jelaskan sendiri dibawah ini contohnya:
```kt
    print("masukan nilai 0 - 100  ")
    var nilai1:Int = readLine()!!.toInt()
    var grade:String

    when(nilai1){
        in 95..100 ->{
           grade ="A"
        }
        else->{
            grade = " bukan A"
        }
    }
    print(grade)
```

### 1.4 When
menaruh wen kedalam nilai variabel
```kt
     print("masukan nilai anda 95 - 100  :  ")
        var nilai:Int = readLine()!!.toInt()
        var cetak:String = when(nilai){
                in 95..100-> "A"
                else-> "bukan A"
        }
        print(cetak)
```


