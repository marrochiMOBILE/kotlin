# Intent 1
bisanya digunakan untuk menuju halaman yang berbeda kalo di html seperti link iya tapi masih kurang tepat

```kotlin
   override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        btn1.setOnClickListener{
            btn1()
        }
    }
    fun btn1(){              // 1      // 2               // 3
        val pindahHalaman = Intent(applicationContext,Main2Activity::class.java)
        pindahHalaman.putExtra("kamu", nilai1.text.toString())
        // 4
        startActivity(pindahHalaman)
    }
```
1. // -> menjalankan pungsi `Intent`
2. // -> bisa diganti dengan `this`, yg artinya main aktiviti yg sedang dijalankan
3. // -> main aktiviti yg dituju 
4. // -> memulai pindah aktiviti dari tempat sekarang ke intent 

> bisa jugha seperti contoh dibawah ini
```php
        Handler().postDelayed({
            startActivity(Intent(this, MainActivity::class.java))
            finish()
        }, 1000)
```
