
# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by: Srinivasan S
Registeration Number : 212220230048
*/
```
## MainActivity.java
```java
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast t2= Toast.makeText(getApplicationContext(),"onCreate Executed",Toast.LENGTH_LONG);
        t2.show();
    }
    protected void onStart(){
        super.onStart();
        Toast t2= Toast.makeText(getApplicationContext(),"onStart Executed",Toast.LENGTH_LONG);
        t2.show();
    }
    protected void onResume(){
        super.onResume();
        Toast t2= Toast.makeText(getApplicationContext(),"onResume Executed",Toast.LENGTH_LONG);
        t2.show();
    }
    protected void onPause(){
        super.onPause();
        Toast t2= Toast.makeText(getApplicationContext(),"onPause Executed",Toast.LENGTH_LONG);
        t2.show();
    }
    protected void onRestart(){
        super.onRestart();
        Toast t2= Toast.makeText(getApplicationContext(),"onRestart Executed",Toast.LENGTH_LONG);
        t2.show();
    }
    protected void onStop(){
        super.onStop();
        Toast t2= Toast.makeText(getApplicationContext(),"onStop Executed",Toast.LENGTH_LONG);
        t2.show();
    }
    protected void onDestroy(){
        super.onDestroy();
        Toast t2= Toast.makeText(getApplicationContext(),"onDestory Executed",Toast.LENGTH_LONG);
        t2.show();
    }
}
```
## activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT
![image](https://user-images.githubusercontent.com/103049243/192280506-ffa6577a-844f-468e-9066-1fea698b79c7.png)
![image](https://user-images.githubusercontent.com/103049243/192280591-7a2c7192-13dc-4524-a604-693bed76196e.png)
![image](https://user-images.githubusercontent.com/103049243/192280703-2cd6796a-ac9a-48ce-b83a-11c473935a7f.png)
![image](https://user-images.githubusercontent.com/103049243/192280793-4e54e74f-d599-49ce-8966-62b97a1f2f47.png)

## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
