Here is the corrected version of the XML files without line numbers:

### TableLayout XML:
```xml
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TableRow android:layout_width="match_parent" android:layout_height="wrap_content">
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Time" />
        <TextClock
            android:id="@+id/textClock"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_marginLeft="20dp" />
    </TableRow>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="First Name" />
        <EditText
            android:id="@+id/editText"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_marginLeft="20dp"
            android:ems="13" />
    </TableRow>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Last Name" />
        <EditText
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_marginLeft="30dp" />
    </TableRow>

    <TableRow>
        <RatingBar
            android:id="@+id/ratingBar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="2" />
    </TableRow>

    <TableRow android:layout_width="fill_parent" android:layout_height="fill_parent">
        <Button
            android:id="@+id/button"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:text="Submit" />
    </TableRow>

</TableLayout>
```

### RelativeLayout XML:
```xml
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".Learning_RelativeLayout">

    <TextView
        android:id="@+id/ET1"
        android:layout_centerHorizontal="true"
        android:layout_centerVertical="false"
        android:layout_centerInParent="false"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Relative Layout!!"
        android:textSize="20dp"
        android:textStyle="bold"
        android:textColor="@android:color/holo_blue_dark" />

    <Button
        android:id="@+id/btnadd"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/ET1"
        android:layout_marginLeft="100dp"
        android:text="+" />

    <Button
        android:id="@+id/btnSub"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@id/ET1"
        android:layout_toRightOf="@+id/btnadd"
        android:layout_marginLeft="20dp"
        android:text="−" />

    <Button
        android:id="@+id/btnMul"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/btnadd"
        android:layout_alignStart="@+id/btnadd"
        android:text="*" />

    <Button
        android:id="@+id/btnDiv"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/btnSub"
        android:layout_toRightOf="@+id/btnMul"
        android:layout_alignStart="@+id/btnSub"
        android:text="/" />

    <Button
        android:id="@+id/btnEqual"
        android:layout_width="27dp"
        android:layout_height="wrap_content"
        android:layout_below="@+id/btnMul"
        android:layout_alignStart="@+id/btnMul"
        android:layout_alignEnd="@+id/btnDiv"
        android:layout_marginStart="84dp"
        android:layout_marginEnd="85dp"
        android:text="=" />

</RelativeLayout>
``` 

This should work properly in your Android project. Let me know if you need further adjustments!
