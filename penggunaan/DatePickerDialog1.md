# DatePickerDialog 1
untuk menampilkan tanggal menggunakan date picker. pertama kita akan membuat 2 kelas. yaitu kelas konstanta dan kelas main utama

###  kelas konstanta
```kt
import java.util.*

class Constanta {

    companion object{
        var calenderOchi: Calendar = Calendar.getInstance()
        var tahun = calenderOchi.get(Calendar.YEAR)
        var bulan = calenderOchi.get(Calendar.MONTH)
        var hari = calenderOchi.get(Calendar.DAY_OF_MONTH)
    }
}
```


#### kelas main utama
```kt
    var datePickerDialogOchi = DatePickerDialog(this, DatePickerDialog.OnDateSetListener { view, year, month, dayOfMonth ->
            tanggal = "$year-${month+1}-$dayOfMonth"
                Log.e("_log tanggal", tanggal)
            tanggalLahir.setText(tanggal.toString())
        } ,Constanta.tahun, Constanta.bulan, Constanta.hari)

        tanggalLahir.setOnClickListener {
            datePickerDialogOchi.show()
        }
```
tanggal disitu adalah atribut `var tanggal:String?=null`
