# setImageResource 1
menseting src gambar
```kotlin
private fun roolDice(){
       val Img :ImageView = findViewById(R.id.images_dice)
        val imgRes = when(Random().nextInt(6)+1){
            1 -> R.drawable.dice_1
            2 -> R.drawable.dice_2
            3 -> R.drawable.dice_3
            4 -> R.drawable.dice_4
            5 -> R.drawable.dice_5
            else -> R.drawable.dice_6
        }
        Img.setImageResource(imgRes)
    }
}
```
1. when()    -> sama ke if else
1. Random()  -> menampilkan secara random
1. nextInt() -> membatasi parameter(6) jadi tidak lebih dari 6 dan dimulai dari 0 maka ditambah + 1
1. dice1/2/3/dst -> gambar
