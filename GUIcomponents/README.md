# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:


## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by:Prem Ananth G
Registeration Number :212220220029
*/
```
## Activity_main.xml:-
```
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:app="http://schemas.android.com/apk/res-auto"

xmlns:tools="http://schemas.android.com/tools"

android:layout_width="match_parent"

android:layout_height="match_parent"

tools:context=".MainActivity">

<Button   
    android:id="@+id/colorButton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_centerHorizontal="true"
    android:layout_marginStart="120dp"
    android:text="Change Color"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/fontButton"
    app:layout_constraintVertical_bias="0.082" />

<Button
    android:id="@+id/fontButton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_below="@id/colorButton"
    android:layout_centerHorizontal="true"
    android:layout_marginStart="120dp"
    android:layout_marginTop="120dp"
    android:text="Change Font"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/textView" />

<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_below="@id/fontButton"
    android:layout_centerHorizontal="true"
    android:text="Hello World!"
    android:textSize="40sp"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.435"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintVertical_bias="0.325" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java:-
```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;

import android.graphics.Typeface;

import android.os.Bundle;

import android.view.View;

import android.widget.Button;

import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

private Button colorButton;

private Button fontButton;

private TextView textView;

@Override

protected void onCreate(Bundle savedInstanceState) {

    super.onCreate(savedInstanceState);
    
    setContentView(R.layout.activity_main);
    
    colorButton = findViewById(R.id.colorButton);
    
    fontButton = findViewById(R.id.fontButton);
    
    textView = findViewById(R.id.textView);
    
    colorButton.setOnClickListener(new View.OnClickListener() {
    
        @Override
        
        public void onClick(View v) {
        
            changeTextColor();
            
        } });

    fontButton.setOnClickListener(new View.OnClickListener() {
    
        @Override
        
        public void onClick(View v) {
        
            changeFont();
            
        }
    });
}
private void changeTextColor() {

    int randomColor = Color.rgb(
    
            (int) (Math.random() * 256),
            
            (int) (Math.random() * 256),
            
            (int) (Math.random() * 256)
    );
    textView.setTextColor(randomColor);
}
private void changeFont() {

    Typeface[] fontStyles = new Typeface[]{
    
            Typeface.DEFAULT,
            
            Typeface.DEFAULT_BOLD,
            
            Typeface.MONOSPACE,
            
            Typeface.SANS_SERIF,
            
            Typeface.SERIF
            
    };

    int randomIndex = (int) (Math.random() * fontStyles.length);
    Typeface selectedFont = fontStyles[randomIndex];
    textView.setTypeface(selectedFont);}
}
```

## OUTPUT

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/74631d3e-06aa-4020-a817-6b45ac86e9aa)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/05aa72e5-6d2e-4aee-957b-7e38c282002f)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/6f83ab04-6f02-44d4-ba5e-03b20eeb7663)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/f77cf83d-1bbb-493c-9e70-83b896a10151)



## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


