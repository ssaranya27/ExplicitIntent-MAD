# Ex.No:2a To develop program to create a text field and a buttons “Explicit Intent". When you click /press Explicit button it should open Second Screen  and print message as" This is Second Activity" 

## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by:
Registeration Number :
*/
```

MainActivity.Java

```
package com.example.intentdemo;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {

    Button btnExplicit;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        btnExplicit = findViewById(R.id.btnExplicit);

        btnExplicit.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MainActivity.this, SecondActivity.class);
                startActivity(intent);
            }
        });
    }
}
```
SecondActivity.java

```
package com.example.intentdemo;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class SecondActivity extends AppCompatActivity {

    Button btnBack;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_second);

        btnBack = findViewById(R.id.btnBack);

        btnBack.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(SecondActivity.this, MainActivity.class);
                startActivity(intent);
                finish(); 
            }
        });


        btnBack.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                finish();
            }
        });

    }
}
```

activity_main.xml

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFF3E0"
    android:padding="20dp">

    <TextView
        android:id="@+id/tvTitle"
        android:layout_width="225dp"
        android:layout_height="73dp"
        android:layout_alignParentStart="true"
        android:layout_alignParentEnd="true"
        android:layout_marginStart="69dp"
        android:layout_marginTop="50dp"
        android:layout_marginEnd="97dp"
        android:fontFamily="sans-serif-medium"
        android:text="This is First Page"
        android:textColor="#D84315"
        android:textSize="24sp"
        android:textStyle="bold" />

    <EditText
        android:id="@+id/etInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/tvTitle"
        android:layout_marginTop="195dp"
        android:background="@android:drawable/edit_text"
        android:hint="Enter something..."
        android:padding="10dp"
        android:textColor="#000000" />

    <Button
        android:id="@+id/btnExplicit"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentStart="true"
        android:layout_alignParentEnd="true"
        android:layout_alignParentBottom="true"
        android:layout_marginStart="92dp"
        android:layout_marginEnd="109dp"
        android:layout_marginBottom="146dp"
        android:backgroundTint="#1976D2"
        android:text="Explicit Intent"
        android:textColor="#FFFFFF"
        android:textSize="18sp" />

</RelativeLayout>
```
activity_second.xml

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#E0F7FA"
    android:padding="20dp">

    <TextView
        android:id="@+id/tvSecond"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="This is Second Activity"
        android:textSize="24sp"
        android:textColor="#00796B"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="100dp"
        android:textStyle="bold"
        android:fontFamily="sans-serif-medium"/>

    <Button
        android:id="@+id/btnBack"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Back to First Page"
        android:textColor="#FFFFFF"
        android:textSize="18sp"
        android:layout_below="@id/tvSecond"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="50dp"
        android:backgroundTint="#D32F2F"/>
</RelativeLayout>
```
AndroidManifest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.Intentdemo">

        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

        <activity
            android:name=".SecondActivity"
            android:exported="true" />

    </application>

</manifest>
```

## OUTPUT

<img width="1920" height="1080" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/267fcaad-97c8-4953-9463-4ef2cfdc5516" />

<img width="1920" height="1080" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/3a8b7d81-1a9c-4fcb-b7c0-6dbb22f67bfe" />


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


