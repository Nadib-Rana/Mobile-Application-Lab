Here is the code you provided with the line numbers removed:

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="50dp"
        android:orientation="horizontal">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Name: "
            android:textSize="15sp" />

        <EditText
            android:id="@+id/ename"
            android:layout_width="match_parent"
            android:layout_height="wrap_content" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="25dp"
        android:orientation="horizontal">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="College: "
            android:textSize="15sp" />

        <EditText
            android:id="@+id/ecollege"
            android:layout_width="match_parent"
            android:layout_height="wrap_content" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginTop="25dp"
        android:gravity="center"
        android:orientation="horizontal">

        <Button
            android:id="@+id/binsert"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginEnd="10dp"
            android:text="Insert" />

        <Button
            android:id="@+id/bdisplay"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginEnd="10dp"
            android:text="Display" />

        <Button
            android:id="@+id/bexit"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Exit" />
    </LinearLayout>
</LinearLayout>
```

The line numbers have been removed as requested. Let me know if you need further adjustments!


Here is your code with the line numbers removed as requested:

```java
package com.example.something;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.database.sqlite.SQLiteDatabase;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    EditText ename, ecollege;
    Button binsert, bexit, bdisplay;
    String nam, coll;
    SQLiteDatabase db;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        ename = findViewById(R.id.ename);
        ecollege = findViewById(R.id.ecollege);
        binsert = findViewById(R.id.binsert);
        bdisplay = findViewById(R.id.bdisplay);
        bexit = findViewById(R.id.bexit);

        db = openOrCreateDatabase("Mydb", MODE_PRIVATE, null);
        db.execSQL("CREATE TABLE IF NOT EXISTS student(name VARCHAR, college VARCHAR);");

        binsert.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                nam = ename.getText().toString();
                coll = ecollege.getText().toString();
                db.execSQL("INSERT INTO student VALUES('" + nam + "','" + coll + "');");
                Toast.makeText(getApplicationContext(), "Row Inserted", Toast.LENGTH_SHORT).show();
            }
        });

        bdisplay.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent = new Intent(getApplicationContext(), PreviewActivity.class);
                startActivity(intent);
                finish();
            }
        });

        bexit.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                System.exit(0);
            }
        });
    }
}
```

Let me know if you need any further adjustments!




