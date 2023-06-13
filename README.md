# Ex_8_CheckBox
Develop a program to create a option menu using checkboxes and display the toast selected checkboxes with Android Studio
## AIM:
To Develop a program for creating a option menu using checkboxes and display the toast selected checkboxes with Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Once the Selected check box displayed to the user processed in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to create an Option Menu
Developed by: Easwar J
RegisterNumber: 212221230024
*/
```

## MainActivity.java:

```
package com.example.ex_8;

import androidx.appcompat.app.AppCompatActivity;
import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    private CheckBox chkAndroid, chkJava, chkPhp, chkCpp, chkC;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        chkAndroid = findViewById(R.id.chkAndroid);
        chkJava = findViewById(R.id.chkJava);
        chkPhp = findViewById(R.id.chkPhp);
        chkCpp = findViewById(R.id.chkCpp);
        chkC = findViewById(R.id.chkC);
    }
    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkAndroid.isChecked())
            selected += "Android";

        if(chkJava.isChecked())
            selected += "\nJava";

        if(chkPhp.isChecked())
            selected += "\nPHP";

        if(chkCpp.isChecked())
            selected += "\nCPP";

        if(chkC.isChecked())
            selected += "\nC";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```


## activity_main.xml:
```

package com.example.ex_8;

import androidx.appcompat.app.AppCompatActivity;
import android.view.View;
import android.widget.CheckBox;
import android.widget.Toast;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    private CheckBox chkAndroid, chkJava, chkPhp, chkCpp, chkC;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        chkAndroid = findViewById(R.id.chkAndroid);
        chkJava = findViewById(R.id.chkJava);
        chkPhp = findViewById(R.id.chkPhp);
        chkCpp = findViewById(R.id.chkCpp);
        chkC = findViewById(R.id.chkC);
    }
    public void showSelected(View view) {

        String selected = "You selected: \n";

        if(chkAndroid.isChecked())
            selected += "Android";

        if(chkJava.isChecked())
            selected += "\nJava";

        if(chkPhp.isChecked())
            selected += "\nPHP";

        if(chkCpp.isChecked())
            selected += "\nCPP";

        if(chkC.isChecked())
            selected += "\nC";

        Toast.makeText(MainActivity.this, selected, Toast.LENGTH_SHORT).show();
    }
}
```

## AndroidMainfest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:supportsRtl="true"
        android:theme="@style/Theme.Ex_8"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```
## Output

![output](https://github.com/jithendra2004/Ex_8_CheckBox/blob/main/j81.png)


## Result:
Thus a Simple Android Application to create an check box and display the selected check box using Android Studio was developed and executed successfully.
