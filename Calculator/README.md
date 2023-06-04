# Ex.No:9 Develop a simple calculator using android studio.

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “calculator operation”.
Developed by: Prem Ananth G
Registeration Number : 212220220029
*/
```
**activity_main.xml : **
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
	xmlns:android="http://schemas.android.com/apk/res/android"
	xmlns:app="http://schemas.android.com/apk/res-auto"
	xmlns:tools="http://schemas.android.com/tools"
	android:layout_width="match_parent"
	android:layout_height="match_parent"
	android:background="#8BC34A"
	android:backgroundTint="@android:color/darker_gray"
	tools:context=".MainActivity">

	<!-- Text View to display our basic heading of "calculator"-->
	<TextView
		android:layout_width="194dp"
		android:layout_height="43dp"
		android:layout_marginStart="114dp"
		android:layout_marginLeft="114dp"
		android:layout_marginTop="58dp"
		android:layout_marginEnd="103dp"
		android:layout_marginRight="103dp"
		android:layout_marginBottom="502dp"
		android:scrollbarSize="30dp"
		android:text=" Calculator"
		android:textAppearance="@style/TextAppearance.AppCompat.Body1"
		android:textSize="30dp"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- Edit Text View to input the values -->
	<EditText
		android:id="@+id/num1"
		android:layout_width="364dp"
		android:layout_height="28dp"
		android:layout_marginStart="72dp"
		android:layout_marginTop="70dp"
		android:layout_marginEnd="71dp"
		android:layout_marginBottom="416dp"
		android:background="@android:color/white"
		android:ems="10"
		android:onClick="clearTextNum1"
		android:inputType="number"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- Edit Text View to input 2nd value-->
	<EditText
		android:id="@+id/num2"
		android:layout_width="363dp"
		android:layout_height="30dp"
		android:layout_marginStart="72dp"
		android:layout_marginTop="112dp"
		android:layout_marginEnd="71dp"
		android:layout_marginBottom="374dp"
		android:background="@android:color/white"
		android:ems="10"
		android:onClick="clearTextNum2"
		android:inputType="number"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- Text View to display result -->
	<TextView
		android:id="@+id/result"
		android:layout_width="356dp"
		android:layout_height="71dp"
		android:layout_marginStart="41dp"
		android:layout_marginTop="151dp"
		android:layout_marginEnd="48dp"
		android:layout_marginBottom="287dp"
		android:background="@android:color/white"
		android:text="result"
		android:textColorLink="#673AB7"
		android:textSize="25sp"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- A button to perform 'sum' operation -->
	<Button
		android:id="@+id/sum"
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:layout_marginStart="16dp"
		android:layout_marginTop="292dp"
		android:layout_marginEnd="307dp"
		android:layout_marginBottom="263dp"
		android:backgroundTint="@android:color/holo_red_light"
		android:onClick="doSum"
		android:text="+"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- A button to perform subtraction operation. -->

	<!-- A button to perform division. -->

	<Button
		android:id="@+id/sub"
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:layout_marginStart="210dp"
		android:layout_marginTop="292dp"
		android:layout_marginEnd="113dp"
		android:layout_marginBottom="263dp"
		android:backgroundTint="@android:color/holo_red_light"
		android:onClick="doSub"
		android:text="-"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintHorizontal_bias="1.0"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent"
		app:layout_constraintVertical_bias="0.507" />

	<Button
		android:id="@+id/div"
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:layout_marginStart="307dp"
		android:layout_marginTop="292dp"
		android:layout_marginEnd="16dp"
		android:layout_marginBottom="263dp"
		android:backgroundTint="@android:color/holo_red_light"
		android:onClick="doDiv"
		android:text="/"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintHorizontal_bias="0.0"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- A button to perform multiplication. -->
	<Button
		android:id="@+id/mul"
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:layout_marginStart="16dp"
		android:layout_marginTop="356dp"
		android:layout_marginEnd="307dp"
		android:layout_marginBottom="199dp"
		android:backgroundTint="@android:color/holo_red_light"
		android:onClick="doMul"
		android:text="x"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent" />

	<!-- A button to perform a modulus function. -->

	<!-- A button to perform a power function. -->

	<Button
		android:id="@+id/button"
		android:layout_width="103dp"
		android:layout_height="46dp"
		android:layout_marginStart="113dp"
		android:layout_marginTop="356dp"
		android:layout_marginEnd="206dp"
		android:layout_marginBottom="199dp"
		android:backgroundTint="@android:color/holo_red_light"
		android:onClick="doMod"
		android:text="%(mod)"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent"
		app:layout_constraintVertical_bias="0.515" />

	<Button
		android:id="@+id/pow"
		android:layout_width="wrap_content"
		android:layout_height="wrap_content"
		android:layout_marginStart="113dp"
		android:layout_marginTop="292dp"
		android:layout_marginEnd="210dp"
		android:layout_marginBottom="263dp"
		android:backgroundTint="@android:color/holo_red_light"
		android:onClick="doPow"
		android:text="n1^n2"
		app:layout_constraintBottom_toBottomOf="parent"
		app:layout_constraintEnd_toEndOf="parent"
		app:layout_constraintHorizontal_bias="0.0"
		app:layout_constraintStart_toStartOf="parent"
		app:layout_constraintTop_toTopOf="parent"
		app:layout_constraintVertical_bias="0.507" />

</androidx.constraintlayout.widget.ConstraintLayout>

**MainActivity.java : **
package com.example.calculator2;

import android.os.Bundle;

import com.google.android.material.snackbar.Snackbar;

import androidx.appcompat.app.AppCompatActivity;

import android.text.TextUtils;
import android.view.View;

import androidx.navigation.NavController;
import androidx.navigation.Navigation;
import androidx.navigation.ui.AppBarConfiguration;
import androidx.navigation.ui.NavigationUI;

import com.example.calculator2.databinding.ActivityMainBinding;

import android.view.Menu;
import android.view.MenuItem;

import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

	private AppBarConfiguration appBarConfiguration;
	private ActivityMainBinding binding;
	public EditText e1, e2;
	TextView t1;
	int num1, num2;

	public boolean getNumbers() {

		//checkAndClear();
		// defining the edit text 1 to e1
		e1 = (EditText) findViewById(R.id.num1);

		// defining the edit text 2 to e2
		e2 = (EditText) findViewById(R.id.num2);

		// defining the text view to t1
		t1 = (TextView) findViewById(R.id.result);

		// taking input from text box 1
		String s1 = e1.getText().toString();

		// taking input from text box 2
		String s2 = e2.getText().toString();



		if(s1.equals("Please enter value 1") && s2.equals(null))
		{
			String result = "Please enter value 2";
			e2.setText(result);
			return false;
		}
		if(s1.equals(null) && s2.equals("Please enter value 2"))
		{
			String result = "Please enter value 1";
			e1.setText(result);
			return false;
		}
		if(s1.equals("Please enter value 1") || s2.equals("Please enter value 2"))
		{
			return false;
		}

		if((!s1.equals(null) && s2.equals(null))|| (!s1.equals("") && s2.equals("")) ){

			String result = "Please enter value 2";

			e2.setText(result);
			return false;
		}
		if((s1.equals(null) && !s2.equals(null))|| (s1.equals("") && !s2.equals("")) ){
			//checkAndClear();
			String result = "Please enter value 1";
			e1.setText(result);
			return false;
		}
		if((s1.equals(null) && s2.equals(null))|| (s1.equals("") && s2.equals("")) ){
			//checkAndClear();
			String result1 = "Please enter value 1";
			e1.setText(result1);
			String result2 = "Please enter value 2";
			e2.setText(result2);
			return false;
		}

		else {
			// converting string to int.
			num1 = Integer.parseInt(s1);

			// converting string to int.
			num2 = Integer.parseInt(s2);


		}

		return true;
	}

	public void doSum(View v) {

		// get the input numbers
		if (getNumbers()) {
			int sum = num1 + num2;
			t1.setText(Integer.toString(sum));
		}
	else
		{
			t1.setText("Error Please enter Required Values");
		}

	}
	public void clearTextNum1(View v) {

		// get the input numbers
	e1.getText().clear();
	}
	public void clearTextNum2(View v) {

		// get the input numbers
		e2.getText().clear();
	}
	public void doPow(View v) {

		//checkAndClear();
		// get the input numbers
		if (getNumbers()) {
			double sum = Math.pow(num1, num2);
			t1.setText(Double.toString(sum));
		}
		else
		{
			t1.setText("Error Please enter Required Values");
		}
	}

	// a public method to perform subtraction
	public void doSub(View v) {
		//checkAndClear();
		// get the input numbers
		if (getNumbers()) {
			int sum = num1 - num2;
			t1.setText(Integer.toString(sum));
		}
		else
		{
			t1.setText("Error Please enter Required Values");
		}
	}

	// a public method to perform multiplication
	public void doMul(View v) {
		//checkAndClear();
		// get the input numbers
		if (getNumbers()) {
			int sum = num1 * num2;
			t1.setText(Integer.toString(sum));
		}
		else
		{
			t1.setText("Error Please enter Required Values");
		}
	}

	// a public method to perform Division
	public void doDiv(View v) {
		//checkAndClear();
		// get the input numbers
		if (getNumbers()) {

			// displaying the text in text view assigned as t1
			double sum = num1 / (num2 * 1.0);
			t1.setText(Double.toString(sum));
		}
		else
		{
			t1.setText("Error Please enter Required Values");
		}
	}

	// a public method to perform modulus function
	public void doMod(View v) {
		//checkAndClear();
		// get the input numbers
		if (getNumbers()) {
			double sum = num1 % num2;
			t1.setText(Double.toString(sum));
		}
		else
		{
			t1.setText("Error Please enter Required Values");
		}
	}


	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_main);
		e1 = (EditText) findViewById(R.id.num1);
		// defining the edit text 2 to e2
		e2 = (EditText) findViewById(R.id.num2);
	}

	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		// Inflate the menu; this adds items to the action bar if it is present.
		getMenuInflater().inflate(R.menu.menu_main, menu);
		return true;
	}

	@Override
	public boolean onOptionsItemSelected(MenuItem item) {
		// Handle action bar item clicks here. The action bar will
		// automatically handle clicks on the Home/Up button, so long
		// as you specify a parent activity in AndroidManifest.xml.
		int id = item.getItemId();

		//noinspection SimplifiableIfStatement
		if (id == R.id.action_settings) {
			return true;
		}

		return super.onOptionsItemSelected(item);
	}

	@Override
	public boolean onSupportNavigateUp() {
		NavController navController = Navigation.findNavController(this, R.id.nav_host_fragment_content_main);
		return NavigationUI.navigateUp(navController, appBarConfiguration)
				|| super.onSupportNavigateUp();
	}
}

## OUTPUT

![Screenshot-2119](https://github.com/PremAnanth2002/Mobile-Application-Development/assets/112572885/fc9bbcd8-569d-4e31-9ccd-819f8a8feb92)



## RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.
