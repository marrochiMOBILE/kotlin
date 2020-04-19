# ScreenSplash 1
buatlah dua main aktivity di app>java>com.example.namaProject>
 1. MainActivity
 1. screenSplasher
 
> kalo kalian bingung buat aktiviti baru kalian bisa ikut contoh dibawah ini
```
1.app>res>drawable klik kanan 
2.pilih new>Activity>Empty Activity 
```
#### kemudian ke app>manifest>AndroidManifest.xml
```xml
 <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/AppTheme">
        // urutan 1 yg dijadikan plasher
        <activity android:name=".screenSplasher" android:theme="@style/Theme.AppCompat.NoActionBar">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        // urutan 2 main utama
        <activity android:name=".MainActivity"></activity>
    </application>
```
#### kemudian ke app>java>com.example.namaProject>screenSplasher.kt/screenSplasher
```kotlin
package com.example.latihan2_rumusrumussederhana

import android.content.Intent
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.os.Handler

class screenSplasher : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_screen_splasher)
          
        Handler().postDelayed({
            startActivity(Intent(this, MainActivity::class.java))
            finish()
        }, 1000)
    }
}

```
1. Handler().postDelayed({}) | 1paket -> yaitu untuk menentukan delay
1. startActivity(Intent()) -> untuk memulai star halaman
1. this -> halaman sekarang yaitu screenSplasher
1. MainActivity::class.java -> dipindahkan ke halaman MainActivity
1. 1000 -> waktu itungan milisecond 1000 = 1 detik

