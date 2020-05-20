# Random 1
dari namanya saja sudah jelas bukan, disini ada contoh menggunakan methdod Random() dengan menggunakan bantuan when
```kt
// variable global dengan menggunakan lateinit
 lateinit var  rollBtn:Button
 
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        // binding init
        var bindings: ActivityMainBinding = DataBindingUtil.setContentView(this,R.layout.activity_main)
        
        rollBtn = findViewById(R.id.roll_btn)
        
        bindings.rollBtn.setOnClickListener{
            roolDice()
        }
    }

    private fun roolDice(){
        val Img :ImageView = findViewById(R.id.images_dice)
        val imgRes = when(Random().nextInt(6)+1){ // kenapa ada +1 karena index dimulai dari 0
            1 -> R.drawable.dice_1
            2 -> R.drawable.dice_2
            3 -> R.drawable.dice_3
            4 -> R.drawable.dice_4
            5 -> R.drawable.dice_5
            else -> R.drawable.dice_6
        }
        Img.setImageResource(imgRes) // untuk menseting ulang gambar
    }
```
