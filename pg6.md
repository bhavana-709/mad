

Xml code


<?xml version="1.0" encoding="utf-8"?>

<ScrollView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="16dp">

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="WELCOME"
            android:textAlignment="center"
            android:textSize="24sp"
            android:textStyle="bold"/>

        <EditText
            android:id="@+id/editTextName"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="Enter your name"/>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Gender"
            android:layout_marginTop="16dp"/>

        <RadioGroup
            android:layout_width="match_parent"
            android:layout_height="wrap_content">

            <RadioButton
                android:id="@+id/radioMale"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Male"/>

            <RadioButton
                android:id="@+id/radioFemale"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Female"/>

        </RadioGroup>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Languages Known"
            android:layout_marginTop="16dp"/>

        <CheckBox
            android:id="@+id/checkEnglish"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="English"/>

        <CheckBox
            android:id="@+id/checkKannada"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Kannada"/>

        <ProgressBar
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            style="?android:attr/progressBarStyleHorizontal"
            android:progress="50"
            android:layout_marginTop="16dp"/>

        <Button
            android:id="@+id/buttonSubmit"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Submit"
            android:layout_marginTop="16dp"/>

        <ImageView
            android:layout_width="200dp"
            android:layout_height="200dp"
            android:layout_gravity="center"
            android:layout_marginTop="16dp"
            android:src="@mipmap/ic_launcher"/>

    </LinearLayout>

</ScrollView>


java code
package com.example.allviewsapp;

import android.os.Bundle;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}

for imade apps,res drawable click file 

if not  copy paste this code;
            android:src="@mipmap/ic_launcher"/>

Enter:
•	Name: AllViewsApp 
•	Language: Java

