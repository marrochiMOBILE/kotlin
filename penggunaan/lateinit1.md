# lateinit 1
bisa dibilang mendklerasikan variabel global
```kotlin

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
```
