# รายงานผลการทดลอง

<ชื่อ-นามสกุล นาย สิขเรศ คุ้มยิ้ม รหัสนักศึกษา 603410220-8>

## คำสั่งการแสดงผลผ่าน Logcat

Debug log

```kotlin
Log.d("TAG", "Message"
```

Error log

```kotlin
Log.e("TAG", "Message")
```

Info log

```kotlin
Log.i("TAG", "Message")
```

Verbose log

```kotlin
Log.v("TAG", "Message")
```

Warning log

```kotlin
Log.w("TAG", "Message")
```

## SNACKBAR และ TOST

คำสั่งแสดง Snackbar

```kotlin
Snackbar.make(View, "-- Snackbar --", Snackbar.LENGTH_SHORT).show()
```

คำสั่งแสดง Tost

```kotlin
Toast.makeText(this,"-- Toast --",Toast.LENGTH_SHORT).show()
```

## Android LiveCycle Activity

จงอธิบาการทำงานของเมธอทต่อไปนี้ ว่าเกิดขึ้นเมื่อใดของโปรแกรม พร้อมแสดงตัวอย่างโค้ดการทำงานของเมธอท (กำหนดให้แสดง log message เมื่อมีการทำงานของเมธอท)

1. onCreate() ->

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        Log.i("onCreate","--- Created Activity ---")
```

2. onStart() ->

```kotlin
override fun onStart() {
        super.onStart()
        Log.i("Ac Start", "Start!!")
        }
```

3. onResume() ->

```kotlin
override fun onResume() {
        super.onResume()
        Log.i("onResume", "Resume!!")
        }
```

4. onPause() ->

```kotlin
override fun onPause() {
        super.onPause()
        Log.i("Ac Pause", "Pause!!")
        }
```

5. onStop() ->

```kotlin
override fun onStop() {
        super.onStop()
        Log.i("Ac Stop", "Stop!!")
        }
```

6. onDestroy() ->

```kotlin
override fun onDestroy() {
        super.onDestroy()
        Log.i("Ac Destroy", "Destroy!!")
        }
```

7. onRestart() ->

```kotlin
override fun onRestart() {
        super.onRestart()
        Log.i("Ac Restart", "onRestart")
        }
```

## Start new Activity

คำสั่งสำหรับเปิด activity ใหม่

```kotlin
var i = Intent(this,Main2Activity::class.java)
            startActivity(i)
```

คำสั่งสำหรับเปิด activity ใหม่ ผ่านเมนู setting

```kotlin
 override fun onOptionsItemSelected(item: MenuItem): Boolean {
        // Handle action bar item clicks here. The action bar will
        // automatically handle clicks on the Home/Up button, so long
        // as you specify a parent activity in AndroidManifest.xml.
        return when (item.itemId) {
            R.id.action_settings -> true
            R.id.action_settings ->{
                Toast.makeText(this,"Menu Click",Toast.LENGTH_SHORT)
                return true
            }
            else -> super.onOptionsItemSelected(item)
        }
    }
```
