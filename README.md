# FinalAppKotlin
import android.icu.text.SimpleDateFormat
import android.icu.util.ULocale.ENGLISH
import android.support.v7.app.AppCompatActivity
import android.os.Bundle
import android.widget.Button
import android.widget.TextView
import java.time.LocalDate
import java.util.*

    class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val txtMessage = findViewById<TextView>(R.id.txtMessage)
        val btnSubmit = findViewById<Button>(R.id.btnSubmit)

        //val date = LocalDate.now()
        //val day = date.getDayOfWeek()

        val day = SimpleDateFormat("EEEE", ENGLISH).format(System.currentTimeMillis())

        btnSubmit.setOnClickListener {
            txtMessage.setText("Today is ${day}, take out your garbage.")
        }
    }
}
