Here is the properly formatted XML layout file for the login page:

```xml
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@android:color/system_notification_accent_color"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <!-- Title for the Login Page -->
    <TextView
        android:id="@+id/textView3"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Log-in Page"
        android:textAlignment="center"
        android:textSize="40dp"
        android:textColor="@color/colorPrimaryDark" />

    <!-- Input for Name -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        
        <TextView
            android:id="@+id/textView4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Enter Name" />
        
        <EditText
            android:id="@+id/etName"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:paddingLeft="10dp"
            android:layout_margin="10dp"
            android:hint="Enter Name Here" />
    </LinearLayout>

    <!-- Input for Password -->
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        
        <TextView
            android:id="@+id/textView5"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Enter Password" />
        
        <EditText
            android:id="@+id/etPass"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPassword"
            android:hint="Enter Password Here" />
    </LinearLayout>

    <!-- Buttons for Submit and Reset -->
    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal">
        
        <Button
            android:id="@+id/btnOk"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Ok" />
        
        <Button
            android:id="@+id/btnReset"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:text="Reset" />
    </LinearLayout>
</LinearLayout>
```

### Key Features:
1. **Login Title:** A `TextView` displays "Log-in Page" with centralized alignment.
2. **Name Input Field:** A `TextView` prompts for the name, paired with an `EditText` for user input.
3. **Password Input Field:** A `TextView` prompts for a password, paired with an `EditText` for secure text input.
4. **Buttons:** Two `Button` components for "Ok" (submit action) and "Reset" (clear fields action).

Make sure the IDs match those used in the Java code (`etName`, `etPass`, `btnOk`, and `btnReset`).
// Code for Intent to switch from login activity to a new activity
package com.example.login;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    EditText ET1, ET2;
    Button B1, B2;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Referencing UI components
        ET1 = (EditText) findViewById(R.id.etName);
        ET2 = (EditText) findViewById(R.id.etPass);
        B1 = (Button) findViewById(R.id.btnOk);
        B2 = (Button) findViewById(R.id.btnReset);

        // Login Button click listener
        B1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Toast.makeText(getApplicationContext(), "Login Button Selected.", Toast.LENGTH_LONG).show();
                String textN = ET1.getText().toString();
                String textP = ET2.getText().toString();

                // Check credentials
                if ((textN.equals("ABC")) && (textP.equals("123"))) {
                    Intent intent = new Intent(getApplicationContext(), temperatureTransformationApplication.class);
                    startActivity(intent); // Switch to the next activity
                }
            }
        });

        // Reset Button click listener
        B2.setOnClickListener(new View.OnClickListener() {
            public void onClick(View v) {
                Toast.makeText(getApplicationContext(), "Reset Button Selected.", Toast.LENGTH_LONG).show();
                // Additional reset logic can go here
            }
        });
    }
}



Here is the code without line numbers:

```java
package com.example.login;

import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class pageTwo extends AppCompatActivity {

    private Button cToF;
    private TextView result;
    private EditText enterTemp;

    double result1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_page_two);

        // Referencing UI components
        cToF = findViewById(R.id.cToF);
        result = findViewById(R.id.result);
        enterTemp = findViewById(R.id.enterTemp);

        // Button click listener for temperature conversion
        cToF.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // Convert input from text to double
                double temp = Double.parseDouble(enterTemp.getText().toString());
                // Celsius to Fahrenheit conversion formula
                result1 = (temp * 1.8) + 32;
                // Display the result in Fahrenheit
                result.setText(String.valueOf(result1));
            }
        });
    }
}
```

### **Key Highlights:**

1. **Temperature Conversion Logic:**
   - Converts a given Celsius temperature to Fahrenheit using the formula:  
     `F = (C × 1.8) + 32`
   - Result is displayed in the `TextView` named `result`.

2. **UI Components Referenced:**
   - `Button`: **cToF**
   - `EditText`: **enterTemp**
   - `TextView`: **result**

3. **Interactive Behavior:**
   - User enters a temperature in Celsius in the `EditText` field.
   - On clicking the button, the converted Fahrenheit value is displayed.

4. **Error Handling (Optional):**
   - Ensure proper input validation (e.g., check if the field is not empty and contains valid numeric input).

### **Input/Output:**
- **Input:**
  - A numeric value (temperature in Celsius) entered in `enterTemp`.
- **Output:**
  - The equivalent temperature in Fahrenheit is displayed in the `result` TextView.
