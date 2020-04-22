# Readline 1

readLine memberi nilai yg akan kita input ke variabel. readline disini menganggap semua yg di input character

```kt
 print("Masukan Nama Anda : ")
    var nama = readLine()
    var namab = readLine()
    
    println("iya nama saya adalah : " + nama +"/$namab") // output yaitu yg diinput 
```

sedangkan untuk penegasan menggunakan `!!` double mari kita licah contoh

```kt
    //sedangkan variabel yg diberi penegasan harus menggunakan tanda seru 2 untuk readLine 'nya
    print("Julukan anda : ")
    var nama2:String = readLine()!!
    println("IYA julukan saya  adalah : " + nama2)
```

anda jugha bisa merubah ke nilai desimal ataupun yg lainya
```kt
    print("masukan umur anda : ")
    var umur:Int = readLine()!!.toInt()
    if(umur <= 25){
        print("umur kamu masih kecil "+umur)
    }
    else if(umur >= 26 && umur <= 34 ){
        print("wah umur kamu ternyata $umur tahun. keliatan dewasa")
    }
    else{
        print("umur kamu dewasa udah $umur")
    }


    println();
    print("masukan angka yg anda mau : ")
    val tes1:Double = readLine()!!.toDouble()
    print("\t $tes1 iy itulah angka anda")
```

catatan :  itu harus menggunakan penegasan `!!` -> **`readLine()!!.toInt()`** 
