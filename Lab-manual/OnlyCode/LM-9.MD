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
