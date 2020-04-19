# isNullOrBlank 1
untuk mengecek apakah EditText sudah terisi apa belom
```kotlin
Variable.isNullOrBlank()
```
contoh lengkapnya
```kotlin
package com.example.latihan2_rumusrumussederhana

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.text.Editable
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

     btnHitung.setOnClickListener {
      val alas = EdTAlas.text.toString()
      val tinggi = EdTTinggi.text.toString()

         if(alas.isNullOrBlank()){
             EdTAlas.error= "tidak boleh kosong"
             EdTAlas.requestFocus()
         }else if(tinggi.isNullOrBlank()){
             EdTTinggi.error= "tidak boleh kosong"
             EdTTinggi.requestFocus()
         }
         else{
             funcHitung(alas.toDouble(), tinggi.toDouble())
         }
     }
    }
    fun funcHitung(alas:Double, tinggi:Double){
        val beritKecil  = alas * tinggi
        abcde.text = beritKecil.toString()
    }

}


```
