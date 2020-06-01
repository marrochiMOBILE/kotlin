# NumberFormat
intinya disini bisa memformat number contoh salah satunya kita akan memformat menjadi uang rupiah.
buat 2 kelas yaitu kelas format rupiah dan main utama.

### kelas format rupiah
```kt
  companion object {
                fun rupiahFormat(number:String) :String{
                val rupiahFormAT = NumberFormat.getInstance(Locale.GERMANY)
                return rupiahFormAT.format(number.toLong())
            }
 }
```

### main utama 
```kt
textSaldo.text = "Rp  " + ConverterOchi.rupiahFormat((Constant.masuk - Constant.keluar).toString())
```

1. textSaldo -> adalah id xml
1. ConverterOchi -> nama kelas format rupiah
1. rupiahFormat -> fungsinya
1. (Constant.masuk - Constant.keluar) -> itu nilainya contoh 10000 - 5000
