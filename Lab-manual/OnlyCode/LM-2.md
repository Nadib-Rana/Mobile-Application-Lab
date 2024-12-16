Here's your Java code without line numbers and adjusted formatting:

```java
package com.example.login;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    EditText etName;
    Button BtnOK;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Referencing
        etName = (EditText) findViewById(R.id.etName);
        BtnOK = (Button) findViewById(R.id.btnOk);
    }
}
```


Here’s your revised Java code without line numbers and formatted appropriately:

```java
package com.example.login;

© Dept. of Computer Science and Engineering, GUB

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    EditText etName;
    Button BtnOK;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Referencing UI components
        etName = (EditText) findViewById(R.id.etName);
        BtnOK = (Button) findViewById(R.id.btnOk);

        // Event Listener
        // Setting event listener for Login Button
        BtnOK.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Toast.makeText(getApplicationContext(), "Login Button Selected.", Toast.LENGTH_LONG).show();
            }
        });
    }
}
```

### Notes:
1. The code is now properly formatted and organized.
2. The event listener for the login button displays a `Toast` message when the button is clicked.
3. Ensure that the IDs `etName` and `btnOk` in your `activity_main.xml` match those in the Java code.
