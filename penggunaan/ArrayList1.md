# ArrayList 1
bisa disebut list array seperti array pada lainya iya..
> menjalankan di editor
```kotlin
    //data berubah menjadi array
    var nilai1 = ArrayList<String>()
    nilai1.add("bambang") // 0
    nilai1.add("julius") // 1
    nilai1.add("rissa") // 2
    nilai1.add("hartono") // 3
    
   //get untuk mendapatkan nilai array yg diminta 0
    print("nama yg tampil adalah " + nilai1.get(0)+"\n")
    
    // val udah fix tidak bisa diubah nilainya dan var bisa diubah
    val nilai1chrono = nilai1.get(1);
    
    //menyeting nilai yg tadinya julius diubah menjadi julius chrono
    nilai1.set(1, "julius chrono");
    print("nilai nama yg sudah di ubah awalnya($nilai1chrono) diganti menjadi -> ${nilai1.get(1)} ")

    println("\n\n\n")
    println("----------------")
    println("daftar nama-nama")
    println("----------------")
    for(item1 in nilai1){

        println(item1)
    }

    println()
    println()
    
   //pake containts untuk mencari nilai array
    print("konsep pencarian  : ")
    var nilai2 = readLine()

    if(nilai1.contains("$nilai2")){
        print("nama sudah terdaftar")
    }
    else{
        print("belom terdaftar")
    }
```
penggunaan dalam android studio
```kotlin
        var daftarNama =  ArrayList<String>()
        daftarNama.add("machiatto")
        daftarNama.add("cafucino")
        daftarNama.add("kapal api")
        daftarNama.add("americano")
        daftarNama.add("chocalate")

        val arrayAdapter = ArrayAdapter(applicationContext,android.R.layout.simple_list_item_1,daftarNama)
        listview.adapter = arrayAdapter;
```
##### `ArrayAdapter()` -> bisa dibilang untuk menampilkan arraylist untuk ditampilkan ke list view
##### ArraAdapter(`disini bisa pake this/applicationContex`t,`androidR.layout.simple_list_item_1/2/dll bnyak variasi kotlin`, `variabel`)
##### `this` -> maksudnya yaitu aktivity tersebut yg sekarang yg sedang dijalankan


