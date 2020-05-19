# ArrayAdapter 1
array adapter untuk menampilkan nilai dari array list contohnya dibawah ini

```kotlin
 var daftarNama =  ArrayList<String>()
        daftarNama.add("machiatto")
        daftarNama.add("cafucino")
        daftarNama.add("kapal api")
        daftarNama.add("americano")
        daftarNama.add("chocalate")
                            // 1           // 2                  //3            // 4            // 5
        val arrayAdapter = ArrayAdapter(applicationContext,android.R.layout.simple_list_item_1,daftarNama)
          // 6      // 7
        listview.adapter = arrayAdapter;
```
1. //  -> menjalankan fungsi array adapter
2. //  -> bisa diganti pake `this` yg artinya main aktiviti yg sedang kita jalankan saat ini
3. //  -> packgae android untuk memanggil method dari layout
4. //  -> berbagai variasi ini salah satunya yg disediakan kotlin
5. //  -> variabel yg menyimpan nilai array list
6. //  -> id listview dengan menggunakan kotlin sintatik
7. //  -> jalankan adapter yg udah ditampung
