# Toast 1
Toast adalah sebuah pesan peringatan yang menghilang dengan sendirinya
```kotlin
Toast.makeText(this,"Tidak Boleh Bernilai 0", Toast.LENGTH_SHORT).show()
```
1. this -> ngikut bae diamah maksudnya ngikut halaman / main_aktivity
1. pesan -> "bebas mau apa aja"
1. waktu -> Toast.LENGTH_SHORT 

> Durasi waktu penampilan toast terdiri dari 2 macam, yaitu:
```
LENGTH_LONG, durasi ini berarti akan menampilkan pesan untuk jangka waktu yang lama.

LENGTH_SHORT, durasi ini berarti akan menampilkan pesan untuk jangka waktu yang singkat.
```
