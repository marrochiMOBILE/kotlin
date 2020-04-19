# putExtra 1
kalo di html bisa dibilang ini atribut `name` yg dikirim lewat post/get
#### 1 aktiviti pertama
```kotlin
  override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        btn1.setOnClickListener{
            btn1()
        }
    }
    fun btn1(){
        val pindahHalaman = Intent(applicationContext,Main2Activity::class.java)
        pindahHalaman.putExtra("kamu", nilai1.text.toString())
        startActivity(pindahHalaman)
    }
```

> putExtra("bebas nama nameenya apa aja", id nilai dari edit text bisanya)
#### 2 aktiviti kedua
kemudian di tangkap 
```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main2)
                                // menangkap data yg dilepmar lewat intent
        val txtNama:String = intent.getStringExtra("kamu")
        txt2.text = txtNama

        btn2.setOnClickListener{
            btn2()
        }
    }

    fun btn2(){
        val pindahHalaman2 = Intent(this,MainActivity::class.java)
        startActivity(pindahHalaman2)
    }
```
