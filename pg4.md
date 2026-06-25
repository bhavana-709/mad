<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="24dp"
    android:background="#EFEFEF">

    <EditText
        android:id="@+id/usr"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Username"
        android:inputType="textPersonName"/>

    <EditText
        android:id="@+id/pwd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="12dp"
        android:hint="Enter Password"
        android:inputType="textPassword"/>

    <Button
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="18dp"
        android:text="Login"
        android:backgroundTint="@android:color/holo_blue_dark"
        android:textColor="#FFFFFF"/>

</LinearLayout>


package com.example.emailapp;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText et1, et2;
    Button buttonLogin;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        et1 = findViewById(R.id.usr);
        et2 = findViewById(R.id.pwd);
        buttonLogin = findViewById(R.id.btn);

        buttonLogin.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                String username = et1.getText().toString().trim();
                String password = et2.getText().toString().trim();

                if (username.isEmpty() || password.isEmpty()) {

                    Toast.makeText(MainActivity.this,
                            "Username or Password is empty",
                            Toast.LENGTH_SHORT).show();

                } else if (username.equals("admin") && password.equals("welcome")) {

                    Toast.makeText(MainActivity.this,
                            "Login Successful",
                            Toast.LENGTH_SHORT).show();

                } else {

                    Toast.makeText(MainActivity.this,
                            "Login Fail",
                            Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}



Username:
admin
Password
welcome
Output
Login Successful
Name : EmailApp
Language : Java
Minimum SDK : API 24
