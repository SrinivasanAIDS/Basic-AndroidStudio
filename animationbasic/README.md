# Ex.No: 9 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as "androidanimation" and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Create a anim folder under res and create the xml files for the animation operators.

Step 7: Add animation operations in MainActivity file.

Step 8: Save and run the application.



## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: Srinivasan S
Registeration Number : 212220230048
*/
```
## MainActivity.java
```java
package com.example.androidanimation;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.view.animation.Animation;
import android.view.animation.AnimationUtils;
import android.widget.ImageView;
import android.view.View;


public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    public void clockwise(View view){
        ImageView image = (ImageView)findViewById(R.id.imageView);
        Animation animation = AnimationUtils.loadAnimation(getApplicationContext(),
                R.anim.myanimation);
        image.startAnimation(animation);
    }

    public void zoom(View view){
        ImageView image = (ImageView)findViewById(R.id.imageView);
        Animation animation1 = AnimationUtils.loadAnimation(getApplicationContext(),
                R.anim.clockwise);
        image.startAnimation(animation1);
    }

    public void fade(View view){
        ImageView image = (ImageView)findViewById(R.id.imageView);
        Animation animation1 =
                AnimationUtils.loadAnimation(getApplicationContext(),
                        R.anim.fade);
        image.startAnimation(animation1);
    }

    public void blink(View view){
        ImageView image = (ImageView)findViewById(R.id.imageView);
        Animation animation1 =
                AnimationUtils.loadAnimation(getApplicationContext(),
                        R.anim.blink);
        image.startAnimation(animation1);
    }

    public void move(View view){
        ImageView image = (ImageView)findViewById(R.id.imageView);
        Animation animation1 =
                AnimationUtils.loadAnimation(getApplicationContext(), R.anim.move);
        image.startAnimation(animation1);
    }

    public void slide(View view){
        ImageView image = (ImageView)findViewById(R.id.imageView);
        Animation animation1 =
                AnimationUtils.loadAnimation(getApplicationContext(), R.anim.slide);
        image.startAnimation(animation1);
    }
}
```
## activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:paddingLeft="20dp"
    android:paddingRight="20dp"
    android:paddingTop="20dp"
    android:paddingBottom="20dp"
    tools:context=".MainActivity">

<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Animation"
    android:id="@+id/textView"
    android:textSize="35dp"
    android:layout_alignParentTop="true"
    android:layout_centerHorizontal="true"
    />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="20dp"
        android:layout_height="100dp"
        android:paddingTop="10dp"
        android:layout_below="@+id/textView"
        android:layout_alignRight="@+id/textView"
        android:layout_alignEnd="@+id/textView"
        android:layout_alignLeft="@+id/textView"
        android:layout_alignStart="@+id/textView"
        app:srcCompat="@android:drawable/btn_star_big_on" />
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="zoom"
        android:id="@+id/button"
        android:layout_below="@+id/imageView"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true"
        android:layout_marginTop="40dp"
        android:onClick="clockwise"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="clockwise"
        android:id="@+id/button2"
        android:layout_alignTop="@+id/button"
        android:layout_centerHorizontal="true"
        android:onClick="zoom"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="fade"
        android:id="@+id/button3"
        android:layout_alignTop="@+id/button2"
        android:layout_alignParentRight="true"
        android:layout_alignParentEnd="true"
        android:onClick="fade"/>

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="blink"
        android:onClick="blink"
        android:id="@+id/button4"
        android:layout_below="@+id/button"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="move"
        android:onClick="move"
        android:id="@+id/button5"
        android:layout_below="@+id/button2"
        android:layout_alignRight="@+id/button2"
        android:layout_alignEnd="@+id/button2"
        android:layout_alignLeft="@+id/button2"
        android:layout_alignStart="@+id/button2" />

    <Button
        android:id="@+id/button6"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button3"
        android:layout_marginStart="21dp"
        android:layout_marginLeft="21dp"
        android:layout_marginTop="4dp"
        android:layout_toEndOf="@+id/textView"
        android:layout_toRightOf="@+id/textView"
        android:onClick="slide"
        android:text="slide" />

</RelativeLayout>
```
## myanimation.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
<scale xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromXScale="0.5"
    android:toXScale="3.0"
    android:fromYScale="0.5"
    android:toYScale="3.0"
    android:duration="5000"
    android:pivotX="50%"
    android:pivotY="50%" >
    </scale>

    <scale xmlns:android="http://schemas.android.com/apk/res/android"
        android:startOffset="5000"
        android:fromXScale="3.0"
        android:toXScale="0.5"
        android:fromYScale="3.0"
        android:toYScale="0.5"
        android:duration="5000"
        android:pivotX="50%"
        android:pivotY="50%" >
        </scale>
        </set>
```
## move.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:interpolator="@android:anim/linear_interpolator"
    android:fillAfter="true">

    <translate
        android:fromXDelta="0%p"
        android:toXDelta="75%p"
        android:duration="700" />
</set>
```
## blink.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">
    <alpha android:fromAlpha="0.0"
        android:toAlpha="1.0"
        android:interpolator="@android:anim/accelerate_interpolator"
        android:duration="500"
        android:repeatMode="reverse"
        android:repeatCount="infinite"/>
</set>
```
## fade.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android"
    android:interpolator="@android:anim/accelerate_interpolator">

    <alpha
        android:duration="1000"
        android:fromAlpha="0"
        android:toAlpha="1" />

    <alpha
        android:duration="1000"
        android:fromAlpha="1"
        android:startOffset="2000"
        android:toAlpha="0" />

</set>
```
## clockwise.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android">

<rotate xmlns:android="http://schemas.android.com/apk/res/android"
    android:fromDegrees="0"
    android:toDegrees="360"
    android:pivotX="50%"
    android:pivotY="50%"
    android:duration="5000" >
    </rotate>

    <rotate xmlns:android="http://schemas.android.com/apk/res/android"
        android:startOffset="5000"
        android:fromDegrees="360"
        android:toDegrees="0"
        android:pivotX="50%"
        android:pivotY="50%"
        android:duration="5000" >
        </rotate>
        </set>
```
## zoom.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android"
    android:fillAfter="true" >

    <scale
        android:duration="500"
        android:fromXScale="1.0"
        android:fromYScale="1.0"
        android:interpolator="@android:anim/linear_interpolator"
        android:toXScale="1.0"
        android:toYScale="0.0" />
</set>
```
## slide.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android"
    android:fillAfter="true" >
    <scale
        android:duration="500"
        android:fromXScale="1.0"
        android:fromYScale="1.0"
        android:interpolator="@android:anim/linear_interpolator"
        android:toXScale="1.0"
        android:toYScale="0.0" />
</set>
```
## OUTPUT
## Original
![image](https://user-images.githubusercontent.com/103049243/204443608-c3c77fa6-78b5-424d-a8a5-2f2b54d40c75.png)

## Zoom
![image](https://user-images.githubusercontent.com/103049243/204443688-a0ce74c1-71f4-4f62-af29-4434cc99fc7d.png)

## Clockwise
![image](https://user-images.githubusercontent.com/103049243/204443732-30f5c278-03c1-493e-b328-f4724169183b.png)

## Fade
![image](https://user-images.githubusercontent.com/103049243/204443817-049bc9e1-a48c-426a-8d3b-6df2816fe6b3.png))

## Blink
![image](https://user-images.githubusercontent.com/103049243/204443861-806a8b67-0bd1-4cc1-9b78-8da057d6c341.png)

## Move
![image](https://user-images.githubusercontent.com/103049243/204443922-8696a0fd-192c-417c-822d-bbe32bec2418.png)

## Slide
![image](https://user-images.githubusercontent.com/103049243/204444021-d898e72e-4b86-49b6-a75f-ac53f0194daa.png)

## RESULT
Thus a Simple Android Application to add animations: Move,blink,fade,clockwise,zoom,slide operations using Android Studio is developed and executed successfully.
