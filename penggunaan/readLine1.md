# readLine 1
readLine memberi nilai yg akan kita input ke variabel. readline disini menganggap semua yg di input character. 

> readLine tanpa penegasan

```kotlin
print("masukan nama : ") 
var nama = readLine() 
print("nama saya adalah $nama ")
```

> readLline penegasan
```kotlin
var nama:String = readLine()!!
```
memakai `!!` untuk penagasan.
```kotlin
var nama:Int = readLine()!!.toInt()
```
begitu pula untuk `double`,`int`,`float` dan yg lainya
