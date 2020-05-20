# fragment 1
fragment adalah anak dari aktivitas iya intinya fragment bisa berjalan jika aktivity itu ada 
```kt
            // memanggil fragment
            val fragmentManajer: FragmentManager = supportFragmentManager 
            val fragmentTransition : FragmentTransaction = fragmentManajer.beginTransaction()
            
            // inisial aktivitas fragment contohnya dibah ini kita mempunyai main class pageOne
            val pageSatu = pageOne() // pageOne disini adalah fragment
            
            // frame layout adalah id dari layout main aktivitas
            fragmentTransition.add(R.id.frame_layoutOchi,pageSatu,pageOne::class.java.simpleName) // pageOne disini adalah fragment
            
           
            fragmentTransition.commit() // baru di commit
```
lebih jelasnya lihat dibawah ini 

## satu
#### MainActivity.kt
```kotlin
package com.example.fragment

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import androidx.fragment.app.FragmentManager
import androidx.fragment.app.FragmentTransaction
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        btnPageOne.setOnClickListener{
            val fragmentManajer: FragmentManager = supportFragmentManager 
            val fragmentTransition : FragmentTransaction = fragmentManajer.beginTransaction()
            val pageSatu = pageOne() // pageOne disini adalah fragment
            fragmentTransition.add(R.id.frame_layoutOchi,pageSatu,pageOne::class.java.simpleName) // pageOne disini adalah fragment
            fragmentTransition.commit() // baru di commit
        }

        btnPageTwo.setOnClickListener{
            val fragmentManajer2: FragmentManager = supportFragmentManager
            val fragmentTransition2 : FragmentTransaction = fragmentManajer2.beginTransaction()
            val pageSatu2 = fageTwo() // pageTwo disini adalah fragment
           fragmentTransition2.add(R.id.frame_layoutOchi,pageSatu2,fageTwo::class.java.simpleName) // pageTwo disini adalah fragment
            fragmentTransition2.commit()
        }
    }
}

```
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <LinearLayout
        android:orientation="horizontal"
        android:layout_marginTop="8dp"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        >

        <Button android:id="@+id/btnPageOne"
           android:layout_width="wrap_content"
           android:layout_height="wrap_content"
           android:text="@string/PageOne"
           android:layout_marginStart="16dp"
           android:layout_marginEnd="16dp" />

        <Button android:id="@+id/btnPageTwo"
           android:layout_width="wrap_content"
           android:layout_height="wrap_content"
           android:text="@string/pagetwo"
           android:layout_marginStart="16dp"
           android:layout_marginEnd="16dp" />

    </LinearLayout>

    <FrameLayout
        android:id="@+id/frame_layoutOchi"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>

</LinearLayout>
```
## kedua
#### pageOne.kt
```kotlin
package com.example.fragment


import android.os.Bundle
import android.text.Editable
import androidx.fragment.app.Fragment
import android.view.LayoutInflater
import android.view.View
import android.view.ViewGroup
import android.widget.EditText
import kotlinx.android.synthetic.main.activity_main.*
import kotlinx.android.synthetic.main.fragment_page_one.*

class pageOne : Fragment() {
    // UI
    override fun onCreateView(inflater: LayoutInflater, container: ViewGroup?, savedInstanceState: Bundle?): View? {
        return inflater.inflate(R.layout.fragment_page_one, container, false)
    }

    // proses
    override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
        super.onViewCreated(view, savedInstanceState)


        BTNpageOne.setOnClickListener{

            val nilaiA  =  EDTpageOneA.text.toString()
            val nilaiB  =  EDTpageOneB.text.toString()

            if(nilaiA.isNullOrBlank()){
                EDTpageOneA.error= "tidak boleh kosong"
                EDTpageOneA.requestFocus()
            }else if(nilaiB.isNullOrBlank()){
                EDTpageOneB.error= "tidak boleh kosong"
                EDTpageOneB.requestFocus()
            }
            else{
                funcHitung(nilaiA.toDouble(), nilaiB.toDouble())
            }
        }
    }

    fun funcHitung(nilaiA:Double, nilaiB:Double){
        val beritKecil  = nilaiA + nilaiB
        TxtViewHasilpageOne.text = beritKecil.toString()
    }

}

```
#### fragment_page_one.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".pageOne"
    android:background="@color/ijo">

  <TextView
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:text="@string/bilanganA"
    android:layout_marginTop="16dp"
    android:layout_marginStart="20dp"
    android:textSize="22dp"
    android:textColor="@color/colorPrimaryDark"  />

    <EditText
     android:id="@+id/EDTpageOneA"
     android:layout_height="wrap_content"
     android:layout_width="200dp"
     android:text="@string/kosong"
        android:layout_marginTop="1dp"
        android:layout_marginStart="140dp"
        android:textSize="22dp"
        />

    <TextView
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        android:text="@string/bilanganB"
        android:layout_marginTop="80dp"
        android:layout_marginStart="20dp"
        android:textSize="22dp"
        android:textColor="@color/colorPrimaryDark"  />

    <EditText
        android:id="@+id/EDTpageOneB"
        android:layout_height="wrap_content"
        android:layout_width="200dp"
        android:text="@string/kosong"
        android:layout_marginTop="60dp"
        android:layout_marginStart="140dp"
        android:textSize="22dp"
        />

    <Button
        android:id="@+id/BTNpageOne"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_gravity="center_horizontal"
        android:layout_marginTop="140dp"
        android:layout_marginLeft="10dp"
        android:layout_marginRight="10dp"
        android:text="@string/jumlah"
        />


    <TextView android:id="@+id/TxtViewHasilpageOne"
        android:layout_width="wrap_content"
     android:layout_height="wrap_content"
     android:text="@string/kosong"
     android:textColor="@color/colorPrimaryDark"
     android:textSize="50dp"
     android:layout_gravity="center"   />
</FrameLayout>
```

## ketiga
#### pageTwo.kt
```kotlin
package com.example.fragment


import android.os.Bundle
import androidx.fragment.app.Fragment
import android.view.LayoutInflater
import android.view.View
import android.view.ViewGroup
import kotlinx.android.synthetic.main.fragment_fage_two.*
import kotlinx.android.synthetic.main.fragment_page_one.*

class fageTwo : Fragment() {

    override fun onCreateView(inflater: LayoutInflater, container: ViewGroup?, savedInstanceState: Bundle?): View? {
        return inflater.inflate(R.layout.fragment_fage_two, container, false)
    }

    // proses
    override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
        super.onViewCreated(view, savedInstanceState)


        BTNpageTwo.setOnClickListener{

            val nilaiA  =  EDTpageTwoA.text.toString()
            val nilaiB  =  EDTpageTwoB.text.toString()

            if(nilaiA.isNullOrBlank()){
                EDTpageOneA.error= "tidak boleh kosong"
                EDTpageOneA.requestFocus()
            }else if(nilaiB.isNullOrBlank()){
                EDTpageOneB.error= "tidak boleh kosong"
                EDTpageOneB.requestFocus()
            }
            else{
                funcHitung(nilaiA.toDouble(), nilaiB.toDouble())
            }
        }
    }

    fun funcHitung(nilaiA:Double, nilaiB:Double){
        val beritKecil  = nilaiA - nilaiB
        TxtViewHasilpageTwo.text = beritKecil.toString()
    }

}

```
#### fragment_page_two.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".fageTwo"
    android:background="@color/kuning">

    <TextView
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        android:text="@string/bilanganA"
        android:layout_marginTop="16dp"
        android:layout_marginStart="20dp"
        android:textSize="22dp"
        android:textColor="@color/colorPrimaryDark"  />

    <EditText
        android:id="@+id/EDTpageTwoA"
        android:layout_height="wrap_content"
        android:layout_width="200dp"
        android:text="@string/kosong"
        android:layout_marginTop="1dp"
        android:layout_marginStart="140dp"
        android:textSize="22dp"
        />

    <TextView
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        android:text="@string/bilanganB"
        android:layout_marginTop="80dp"
        android:layout_marginStart="20dp"
        android:textSize="22dp"
        android:textColor="@color/colorPrimaryDark"  />

    <EditText
        android:id="@+id/EDTpageTwoB"
        android:layout_height="wrap_content"
        android:layout_width="200dp"
        android:text="@string/kosong"
        android:layout_marginTop="60dp"
        android:layout_marginStart="140dp"
        android:textSize="22dp"
        />

    <Button
        android:id="@+id/BTNpageTwo"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_gravity="center_horizontal"
        android:layout_marginTop="140dp"
        android:layout_marginLeft="10dp"
        android:layout_marginRight="10dp"
        android:text="@string/kurang"
        />


    <TextView android:id="@+id/TxtViewHasilpageTwo"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/kosong"
        android:textColor="@color/colorPrimaryDark"
        android:textSize="50dp"
        android:layout_gravity="center"   />
</FrameLayout>
```
