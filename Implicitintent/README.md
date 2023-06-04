# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: Prem Ananth G
Registeration Number : 212220220029
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

<EditText
    android:id="@+id/urlEditText"
    android:layout_width="292dp"
    android:layout_height="67dp"
    android:layout_marginStart="56dp"
    android:layout_marginTop="108dp"
    android:hint="Enter URL"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/navigateButton"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_gravity="center"
    android:text="Navigate"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/urlEditText" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java:-
```
package com.example.implicitintent;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
        editText = (EditText) findViewById(R.id.editText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url=editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```

## OUTPUT

![WhatsApp Image 2023-05-27 at 2 36 46 PM](https://github.com/suryacse05/Mobile-Application-Development/assets/119160414/d2abf611-dec5-481a-9bb4-2cd3b8248494)

![WhatsApp Image 2023-05-27 at 2 36 46 PM (1)](https://github.com/suryacse05/Mobile-Application-Development/assets/119160414/b954e267-8ebc-4be4-8295-2bac7b11ad25)

![WhatsApp Image 2023-05-27 at 2 36 46 PM (2)](https://github.com/suryacse05/Mobile-Application-Development/assets/119160414/0f78e5f1-3e6c-48af-8e92-f5416d19b428)



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.


