# ArrayList 1 

adalah sebuah deretan list array

```kt
   // data berubah menjadi array yg tipe datanya string
    var nilai1 = ArrayList<String>()
```

## add
menambahkan data dengan mengguakan `add()`

```kt
    nilai1.add("bambang") // 0
    nilai1.add("julius") // 1
    nilai1.add("rissa") // 2
    nilai1.add("hartono") // 3
```

## get
untuk mendapatkan nilai array menggunkan `get()` dengan parameternya

```kt
print("nama yg tampil adalah " + nilai1.get(0)+"\n")
```
atau

```kt
val nilai1chrono = nilai1.get(1)
```

## set
menset/merubah nilai value dengan `set()`
```kt
    nilai1.set(1, "julius chrono");
    print("nilai nama yg sudah di ubah awalnya($nilai1chrono) diganti menjadi -> ${nilai1.get(1)} ")
```

## menampilkan semua array dengan for
```kt
    for(item1 in nilai1){

        println(item1)
    }
```

## contains
pake containts untuk mencari nilai array
```kt
 print("konsep pencarian  : ")
    var nilai2 = readLine()

    if(nilai1.contains("$nilai2")){
        print("nama sudah terdaftar")
    }
    else{
        print("belom terdaftar")
    }
```

