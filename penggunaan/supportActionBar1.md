# supportActionBar 1
untuk menambahkan beberpa item di actionbar

### menambahkan title
```kt
       // tittle
        supportActionBar!!.setTitle("Tambah Baru Bosque")
```        

### menambahkan icon back `<-` dan fungsi script
```kt
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_add)

        // tittle
        supportActionBar!!.setTitle("Tambah Baru Bosque")
        // icon back home
        supportActionBar!!.setDisplayHomeAsUpEnabled(true)
    }

    // ketika di klik icon back selesai akrivitas disini
    override fun onSupportNavigateUp(): Boolean {
        finish()
        return super.onSupportNavigateUp()
    }
```kt
