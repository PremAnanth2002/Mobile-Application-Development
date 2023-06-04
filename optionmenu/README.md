# Ex.No:10 To create a option menu to display menu items.


## AIM:

To create a option menu to display menu items using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Studio and create a new project or open an existing project.

Step 2: In the project structure, locate and right-click on the "res" folder.

Step 3: From the context menu, select "New" and then choose "Android Resource File".

Step 4: In the "New Resource File" dialog, enter a name for the file, e.g., "menu_options".

Step 5: Set the Resource type to "Menu" using the dropdown menu.

Step 6: Click the "OK" button to create the menu resource file.

Step 7: Open the newly created menu resource file, "menu_options.xml".

Step 8: Inside the file, define the menu items using XML tags.

Step 9: For each menu item, use the <item> tag and specify attributes such as id, title, and icon.

Step 10: Save the menu resource file.

Step 11: Open the activity class where you want to display the menu.

Step 12: Override the onCreateOptionsMenu method in the activity.

Step 13: Inside the onCreateOptionsMenu method, inflate the menu resource file using getMenuInflater().inflate(R.menu.menu_options, menu);.

Step 14: Override the onOptionsItemSelected method to handle menu item selection.

Step 15: Inside the onOptionsItemSelected method, use a switch statement based on the selected menu item's id to perform specific actions.

## PROGRAM:
```
/*
Program to print the text “optionmenu”.
Developed by: Prem Ananth G
Registeration Number :212220220029
*/
```
## activity_main.xml:-
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:tools="http://schemas.android.com/tools"
          
android:layout_width="match_parent"
          
android:layout_height="match_parent"
          
android:orientation="vertical"
          
android:padding="16dp"
          
tools:context=".MainActivity">

<TextView
    android:id="@+id/messageTextView"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:text="Select an option from the menu"
    android:textSize="25dp" />
```
## MainActivity.java:-
```
package com.example.optionmenu;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.widget.TextView;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
private TextView messageTextView;

@Override
protected void onCreate(Bundle savedInstanceState) {

    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    messageTextView = findViewById(R.id.messageTextView);
}

@Override
public boolean onCreateOptionsMenu(Menu menu) {

    getMenuInflater().inflate(R.menu.options_menu, menu);
    return true;
}

@Override
public boolean onOptionsItemSelected(MenuItem item) {
    int itemId = item.getItemId();

    switch (itemId) {
        case R.id.menu_item_1:
            messageTextView.setText("Option 1 selected");
            return true;
        case R.id.menu_item_2:
            messageTextView.setText("Option 2 selected");
            return true;
        case R.id.menu_item_3:
            messageTextView.setText("Option 3 selected");
            return true;
        default:
            return super.onOptionsItemSelected(item);
    }
}
}
```
## Option_View.xml:-
```
<item
    android:id="@+id/menu_item_1"
    android:title="Option 1"
    android:textSize="25dp"/>
<item
    android:id="@+id/menu_item_2"
    android:title="Option 2"
    android:textSize="25dp"/>
<item
    android:id="@+id/menu_item_3"
    android:title="Option 3"
    android:textSize="25dp"/>
```
## OUTPUT

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/31ebf8d7-0af3-4594-bc3e-6f9f289b3b23)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/775d54f9-31cc-4e09-9fee-3510414e5523)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/742f2597-031b-4cfb-a2bc-b5324b0ade84)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/f46e25c2-cf09-430e-87e5-74b69e37a112)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/c248bff7-d080-441f-967b-be94b2b43bb2)

## RESULT
Thus a Simple Android Application to create a option menu to display menu items using Android Studio is developed and executed successfully.


