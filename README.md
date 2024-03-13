# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
1. Open Android Studio: Launch Android Studio and open your Android project.

2. Locate the XML layout file: GUI components in Android are defined in XML layout files, which can be found in the res/layout directory of your project.

3. Identify the component to alter: Locate the XML code corresponding to the GUI component you want to alter. Each GUI component will have its own XML tag (e.g., <TextView>, <Button>, <EditText>, etc.).

4. Make alterations: You can alter various attributes of the component directly in the XML file. For example:

5. Change the text of a TextView using the android:text attribute.
Modify the appearance of a Button using attributes like android:background, android:textColor, etc.
Adjust the properties of other components based on their respective attributes.
Preview changes: After making alterations, you can preview the changes directly in the Android Studio's layout editor. This allows you to see how the altered GUI components will appear on different devices and screen sizes.

6. Handle component interactions (optional): If your alteration involves handling user interactions, such as button clicks or text input, you'll need to write corresponding Java/Kotlin code to define the behavior. This typically involves:

7. Locating the corresponding activity or fragment file.
8. Identifying the component using its ID (defined in the XML layout file).
9. Implementing event listeners or callback methods to handle user interactions.
Writing logic to respond to user actions, such as updating UI elements, processing input, etc.
10. Test your changes: Run your Android application on an emulator or a physical device to test the alterations you've made to the GUI components. Ensure that the app behaves as expected and that the altered components appear and function correctly.

11. Iterate and refine: If necessary, iterate on the alterations by going back to the XML layout file or the Java/Kotlin code to make further adjustments. Continuously test your changes to ensure a satisfactory user experience.

Commit changes (if using version control): If you're using version control (e.g., Git), commit your changes to the repository with descriptive commit messages.
```

## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: bergin.s
Registeration Number : 212222040025
*/
```


```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.139" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CHANGE FONT SIZE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.192" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="CHANGE COLOR"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button"
        app:layout_constraintVertical_bias="0.312" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

```java
package com.example.guicomponents;

import androidx.appcompat.app.AppCompatActivity;

import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    int ch=1;
    float font=30;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t = (TextView) findViewById(R.id.textView);
        Button b1 = (Button) findViewById(R.id.button);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                t.setTextSize(font);
                font = font+5;
                if(font==50)
                    font=30;
            }
        });
        Button b2 = (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                switch(ch){
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if(ch==7)
                    ch=1;
            }
        });
    }
}
```

## OUTPUT
![Screenshot (421)](https://github.com/ArpanBardhan/GUI-components/assets/119405037/830b9be3-7038-4347-b492-3c7702f6ead6)
![Screenshot (422)](https://github.com/ArpanBardhan/GUI-components/assets/119405037/808948e0-e6ac-4a47-b5e4-a678589c2af5)
![Screenshot (423)](https://github.com/ArpanBardhan/GUI-components/assets/119405037/bc8bb33d-0958-4cb8-b332-e37fc96cc4fe)
![Screenshot (424)](https://github.com/ArpanBardhan/GUI-components/assets/119405037/9eee27c8-1062-4c7a-acfb-685bebd9f787)
![Screenshot (425)](https://github.com/ArpanBardhan/GUI-components/assets/119405037/3180f96f-8ff0-47d3-a9ca-dadf0a79a7b9)




## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


