Java code

package com.example.actionbarapp;

import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;
import androidx.appcompat.widget.Toolbar;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        getMenuInflater().inflate(R.menu.menu_main, menu);
        return true;
    }

    @Override
    public boolean onOptionsItemSelected(MenuItem item) {

        if (item.getItemId() == R.id.action_search) {
            Toast.makeText(this, "Search clicked", Toast.LENGTH_SHORT).show();
            return true;
        }

        if (item.getItemId() == R.id.action_settings) {
            Toast.makeText(this, "Settings clicked", Toast.LENGTH_SHORT).show();
            return true;
        }

        return super.onOptionsItemSelected(item);
    }
}

xml code
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">

    <androidx.appcompat.widget.Toolbar
        android:id="@+id/toolbar"
        android:layout_width="match_parent"
        android:layout_height="?attr/actionBarSize"
        android:background="#6200EE"
        app:title="Menu Example"
        app:titleTextColor="@android:color/white"/>

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Program 7 - Menu"
        android:textSize="22sp"
        android:layout_gravity="center"
        android:layout_marginTop="50dp"/>

</LinearLayout>


Menu code
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item
        android:id="@+id/action_search"
        android:title="Search"
        android:showAsAction="ifRoom" />

    <item
        android:id="@+id/action_settings"
        android:title="Settings"
        android:showAsAction="ifRoom" />

</menu>
Enter:
•	Project Name: ActionBarApp 
•	Language: Java
•	
•	Create menu_main.xml
•	res
   ↓
Right-click on menu
   ↓
New
   ↓
Menu Resource File
   ↓
File Name : menu_main
   ↓
Root Element : menu
   ↓
Click OK

menu
   ↓
menu_main.xml
   ↓
Delete existing code
   ↓
Paste the following XML code
   ↓
Press Ctrl + S to Save
