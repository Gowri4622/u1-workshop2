### NAME : GOWRI M
### REG NO : 212220230019

# <p align="center"> WORKSHOP-2</P>

## AIM:
To show Image file sending data from one activity to another activity screenshot using android studio. 

## EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step-1:Use Android StudioIDE to create an Android application and name it as My App under a 
package com.example.MyApp, with blank Activity. 

Step-2: Modify the default content of res/layout/activity_main.xml file to display the required 
content and design the layout. 

Step-3: Add the following code to src/MainActivity.java 

Step-4: Create an empty activity and add the following code. 

Step-5: Run your application. 


## PROGRAM:

### main activity.java
```java
package com.example.firstproject; 
import android.content.Intent; 
import androidx.appcompat.app.AppCompatActivity; 
import android.os.Bundle; 
import android.view.View; 
import android.widget.Button; 
import android.widget.EditText; 
public class MainActivity extends AppCompatActivity { 
 Button send_button; 
 EditText send_text; 
 @Override 
 protected void onCreate(Bundle savedInstanceState) { 
 super.onCreate(savedInstanceState); 
 setContentView(R.layout.activity_main); 
 send_button = (Button)findViewById(R.id.button); 
 send_text = (EditText)findViewById(R.id.editTextTextPersonName); 
 send_button.setOnClickListener(new View.OnClickListener() { 
 @Override 
 public void onClick(View v) { 
 String str = send_text.getText().toString(); 
 Intent intent = new Intent(getApplicationContext(), MainActivity2.class); 
 intent.putExtra("message_key", str); // start the Intent 
 startActivity(intent); 
 } 
 }); 
 } 
} 
```
### activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
 xmlns:app="http://schemas.android.com/apk/res-auto" 
 xmlns:tools="http://schemas.android.com/tools" 
 android:layout_width="match_parent" 
 android:layout_height="match_parent" 
 tools:context=".MainActivity"> 
 <Button 
 android:id="@+id/button" 
 android:layout_width="wrap_content" 
 android:layout_height="wrap_content" 
 android:text="Send" 
 app:layout_constraintBottom_toBottomOf="parent" 
 app:layout_constraintEnd_toEndOf="parent" 
 app:layout_constraintStart_toStartOf="parent" 
 app:layout_constraintTop_toTopOf="parent" /> 
 <EditText 
 android:id="@+id/editTextTextPersonName" 
 android:layout_width="wrap_content" 
 android:layout_height="wrap_content" 
 android:ems="10" 
 android:inputType="textPersonName" 
 android:text="Name" 
 app:layout_constraintBottom_toBottomOf="parent" 
 app:layout_constraintEnd_toEndOf="parent" 
 app:layout_constraintHorizontal_bias="0.447" 
 app:layout_constraintStart_toStartOf="parent" 
 app:layout_constraintTop_toTopOf="parent" 
 app:layout_constraintVertical_bias="0.161" /> 
</androidx.constraintlayout.widget.ConstraintLayout> 

```
### MainActivity2.java 
```java
package com.example.firstproject; 
import androidx.appcompat.app.AppCompatActivity; 
import android.content.Intent; 
import android.os.Bundle; 
import android.widget.TextView; 
public class MainActivity2 extends AppCompatActivity { 
 TextView receiver_msg; 
 @Override 
 protected void onCreate(Bundle savedInstanceState) 
 { 
 super.onCreate(savedInstanceState); 
 setContentView(R.layout.activity_main2); 
 receiver_msg = (TextView)findViewById(R.id.textView); 
 Intent intent = getIntent(); 
 String str = intent.getStringExtra("message_key"); 
 receiver_msg.setText(str); 
 }}
 ```
 
### Activity_main2.xml 
```java
<?xml version="1.0" encoding="utf-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android" 
 xmlns:app="http://schemas.android.com/apk/res-auto" 
 xmlns:tools="http://schemas.android.com/tools" 
 android:layout_width="match_parent" 
 android:layout_height="match_parent" 
 tools:context=".MainActivity2"> 
 <TextView 
 android:id="@+id/textView" 
 android:layout_width="300dp" 
 android:layout_height="50dp" 
 android:textStyle="bold" 
 android:textSize="40dp" 
 android:layout_marginTop="20dp" 
 android:layout_marginLeft="40dp" 
 tools:layout_editor_absoluteX="220dp" 
 tools:layout_editor_absoluteY="298dp" /> 
</androidx.constraintlayout.widget.ConstraintLayout>
```

## output
![WhatsApp Image 2022-04-26 at 4 01 56 PM](https://user-images.githubusercontent.com/75235455/167265940-594db8d7-6c9f-4daa-8004-d02141db7939.jpeg)
![WhatsApp Image 2022-04-26 at 4 01 57 PM](https://user-images.githubusercontent.com/75235455/167265944-806bf080-4618-458d-afc4-bf2629e36f5d.jpeg)


## Result
Thus a show Image file sending data from one activity to another activity screenshot using android studio is developed and executed successfully.
