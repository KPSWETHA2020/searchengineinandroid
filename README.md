# Ex.No:6 Build a program to create a first display screen of any search engine using Auto Complete Text View.
## AIM:
To develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as auto and click Next.

Step 3: Then select the Empty Activity and click Next. Finally click Finish.

Step 4: Design layout using AutoComplete TextView in activity_main.xml.

Step 5: Display screen of search engine in MainActivity file.

Step 6: Launch an emulator and run the application.

## PROGRAM:
```
/*
Program to print the text “display screen of any search engine”.
Developed by: SwethaK.P
Registeration Number : 212220230053
*/
```

### MainActivity.java
```
package com.example.auto;

import android.graphics.Color;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;

public class MainActivity extends AppCompatActivity {

    String[] bike ={"Ampere","Avon","Atlas","BlackSmith","BMW","CFMoto","Demak","Ducati","EBike","Evolet","GenXt","Hero","Hero Honda","Honda","Hi-Bird","Joy","KTM","Kawaski","Kinetic","Kanda","Mahindra","RK Motors","Royal Enfield","Revolt","Techno","TVS","Yamaha"};
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        //Creating the instance of ArrayAdapter containing list of language names
        ArrayAdapter<String> adapter = new ArrayAdapter<String>
                (this,android.R.layout.select_dialog_item,bike);
        //Getting the instance of AutoCompleteTextView
        AutoCompleteTextView actv =  (AutoCompleteTextView)findViewById(R.id.autoCompleteTextView);
        actv.setThreshold(1);//will start working from first character
        actv.setAdapter(adapter);//setting the adapter data into the AutoCompleteTextView
        actv.setTextColor(Color.RED);
    }
}
```

### activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="331dp"
        android:layout_height="62dp"
        android:text="What is your favourite Bike?"
        android:textColor="#C5082D"
        android:textSize="25sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintHorizontal_bias="0.662"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.14" />

    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView"
        android:layout_width="358dp"
        android:layout_height="55dp"
        android:background="#F3AFB9"
        android:text=""
        android:textColor="@color/black"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.49"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.667" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="286dp"
        android:layout_height="200dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.496"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.378"
        app:srcCompat="@drawable/img" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT

![Screenshot (590)](https://user-images.githubusercontent.com/75235813/169639384-cdb38d6f-7b84-4724-a3f8-e67d359cc9f0.png)

![Screenshot (591)](https://user-images.githubusercontent.com/75235813/169639389-2bdd2407-1b07-4e9e-920b-04bd1c3e3522.png)

![Screenshot (592)](https://user-images.githubusercontent.com/75235813/169639397-45ca6335-99d5-4fea-b8ba-8225c87cb5c6.png)


## RESULT
Thus a Simple Android Application develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio is developed and executed successfully.
