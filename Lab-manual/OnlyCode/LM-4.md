Here is the cleaned-up XML code for your layout:

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/etInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:hint="Enter the text name" />

    <ListView
        android:id="@+id/listFont"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
    </ListView>

</LinearLayout>
```

### Key Features:
1. **EditText**:  
   - Provides an input field for the user to type text.  
   - `hint`: Displays placeholder text *"Enter the text name"* to guide the user.  
   - `inputType`: Limits input to a person name (text).

2. **ListView**:  
   - Displays a list of items dynamically.  
   - Items in the list can be defined and populated programmatically in your `MainActivity`.

### **Usage:**
- You can use the `EditText` to capture user input.
- Use the `ListView` to display a list, such as font names, or any dynamically loaded data. 

### **Code Integration:**
In your Java/Kotlin code:
1. Reference these UI elements by their IDs:  
   - `etInput` for the `EditText`.
   - `listFont` for the `ListView`.

2. Populate the `ListView` using an adapter to bind data. Example:
   ```java
   ArrayAdapter<String> adapter = new ArrayAdapter<>(this, android.R.layout.simple_list_item_1, fontList);
   listFont.setAdapter(adapter);
   ```

Let me know if you need more detailed implementation guidance!





Here's the cleaned-up and well-formatted version of your Java code for better readability and understanding:

```java
package com.example.lab2_182da;

import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Typeface;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.EditText;
import android.widget.ListView;

public class MainActivity extends AppCompatActivity {

    EditText etInput;
    ListView listFont;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Referencing UI components
        listFont = findViewById(R.id.listFont);
        etInput = findViewById(R.id.etInput);

        // Adding font names to the list
        String[] values = new String[] {
            "Angilla Tattoo", 
            "Cantate Beveled", 
            "Krinkes Decor PERSONAL", 
            "Krinkes Regular PERSONAL", 
            "Silent Reaction"
        };

        // Setting up the adapter for the ListView
        ArrayAdapter<String> adapter = new ArrayAdapter<>(
            this, android.R.layout.simple_dropdown_item_1line, values
        );
        listFont.setAdapter(adapter);

        // Handling item click events for the ListView
        listFont.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                String itemValue = (String) listFont.getItemAtPosition(position);

                // Setting font based on the selected item
                String fontPath = null;
                switch (itemValue) {
                    case "Angilla Tattoo":
                        fontPath = "fonts/AngillaTattoo.ttf";
                        break;
                    case "Cantate Beveled":
                        fontPath = "fonts/CantateBeveled.ttf";
                        break;
                    case "Krinkes Decor PERSONAL":
                        fontPath = "fonts/KrinkesDecorPERSONAL.ttf";
                        break;
                    case "Krinkes Regular PERSONAL":
                        fontPath = "fonts/KrinkesRegularPERSONAL.ttf";
                        break;
                    case "Silent Reaction":
                        fontPath = "fonts/SilentReaction.ttf";
                        break;
                }

                if (fontPath != null) {
                    // Apply the selected font to the EditText
                    Typeface tf = Typeface.createFromAsset(getAssets(), fontPath);
                    etInput.setTypeface(tf);
                }
            }
        });
    }
}
```

### Improvements Made:
1. **Switched to `switch-case` for cleaner and more readable conditional font selection.**
2. **Removed unnecessary calls to `etInput.getText().toString()` in each case since it was not being used.**
3. **Proper formatting and indentation** for better readability.

### Key Notes:
- Ensure all font files (`.ttf`) are placed in the `assets/fonts/` directory of your project.
- This code dynamically changes the font of the `EditText` based on the selected font name from the `ListView`.
