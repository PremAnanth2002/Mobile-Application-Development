
# Ex.No:7 Develop an android application to display the place name with image using list view in android studio.


## AIM:

To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the list of item.
Developed by: Prem Ananth G
Registeration Number :212220220029
*/
```
## activity_main.xml:-
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"         
xmlns:tools="http://schemas.android.com/tools"         
android:layout_width="match_parent"         
android:layout_height="match_parent"          
tools:context=".MainActivity">

<ListView
    android:id="@+id/simpleListView"
    android:layout_width="match_parent"
    android:layout_height="300dp"
    android:divider="@color/material_blue_grey_800"
    android:dividerHeight="1dp"
    android:footerDividersEnabled="false" />
 </LinearLayout>
```
## Listview.xml:
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
android:layout_width="match_parent"        
android:layout_height="match_parent">

<ImageView
    android:id="@+id/icon"
    android:layout_width="50dp"
    android:layout_height="50dp" />
<TextView
    android:id="@+id/textView"
    android:layout_width="fill_parent"
    android:layout_height="wrap_content"
    android:layout_gravity="center"
    android:textColor="@color/black" />
 </LinearLayout>
```
## MainActivity:-
```
package com.example.placename;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.ListView;
public class MainActivity extends AppCompatActivity 
{
    ListView simpleList;
    String countryList[] = {"India", "China", "Australia", "America", "Korea", "Hong Kong"};
    int flags[] = {R.drawable.india, R.drawable.china, R.drawable.australia, R.drawable.america,
        R.drawable.korea, R.drawable.hongkong};

    @Override
    protected void onCreate(Bundle savedInstanceState) 
    {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        simpleList = findViewById(R.id.simpleListView);

        CustomAdapter customAdapter = new CustomAdapter(getApplicationContext(), countryList, flags);
        simpleList.setAdapter(customAdapter);
    }
}
```
## CustomAdapter.java:-
```
package com.example.placename;
import android.content.Context;
import android.media.Image;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.BaseAdapter;
import android.widget.ImageView;
import android.widget.TextView;
import java.util.zip.Inflater;
public class CustomAdapter extends BaseAdapter { Context context; String countryList[]; int flags[]; LayoutInflater inflter;

public CustomAdapter(Context applicationContext, String[] countryList, int[] flags) {
    this.context = applicationContext;
    this.countryList = countryList;
    this.flags = flags;
    inflter = (LayoutInflater.from(applicationContext));
}

@Override
public int getCount() {
    return countryList.length;
}

@Override
public Object getItem(int i) {
    return null;
}

@Override
public long getItemId(int i) {
    return 0;
}

@Override
public View getView(int i, View view, ViewGroup viewGroup) {
    view = inflter.inflate(R.layout.listview, null);
    TextView country = (TextView) view.findViewById(R.id.textView);
    ImageView icon = (ImageView) view.findViewById(R.id.icon);
    country.setText(countryList[i]);
    icon.setImageResource(flags[i]);
    return view;
}
}
```
## OUTPUT
![WhatsApp Image 2023-06-02 at 20 06 50](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/25cee06b-3d42-4c45-ba96-a54ee505f246)

![WhatsApp Image 2023-06-02 at 20 06 50](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/24b9acc1-6ade-4598-9892-4fc747acb452)

![WhatsApp Image 2023-06-02 at 20 06 50](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/3c3de8eb-5357-4813-8a01-8cc8e7493985)

![WhatsApp Image 2023-06-02 at 20 06 51](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/cd442830-3c6d-42b9-beff-d6c9542252f6)

![WhatsApp Image 2023-06-02 at 20 06 51](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/e1256e52-5d41-483c-adc6-3bbbdc8346ff)





## RESULT
Thus a Simple Android Application to create and develop the application to display the place name with image using list view in android studio is developed and executed successfully.
