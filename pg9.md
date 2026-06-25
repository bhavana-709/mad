Xml code
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/editName"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Name" />

    <Button
        android:id="@+id/btnSave"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Save Preferences"
        android:layout_marginTop="10dp" />

    <TextView
        android:id="@+id/txtResult"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Hello"
        android:textSize="22sp"
        android:layout_marginTop="20dp" />

</LinearLayout>



Java code
package com.example.userprefapp;

import android.content.SharedPreferences;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText editName;
    Button btnSave;
    TextView txtResult;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editName = findViewById(R.id.editName);
        btnSave = findViewById(R.id.btnSave);
        txtResult = findViewById(R.id.txtResult);

        SharedPreferences prefs = getPreferences(MODE_PRIVATE);

        txtResult.setText("Hello " + prefs.getString("name", ""));

        btnSave.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                prefs.edit()
                        .putString("name", editName.getText().toString())
                        .apply();

                txtResult.setText("Hello " + editName.getText().toString());
            }
        });
    }
}



Project Name : UserPrefApp
↓
Language : Java
