# AdditionOfTwoNum
# ANDROID APPLICATION FOR ADDITION OF TWO NUMBERS
# AIM:
To develop an Android application that accepts two numbers and displays their sum when the Add button is clicked.
# Software Used:
Android Studio
Java
XML
GitHub
# Procedure:
1. Create a new Android Studio project.
2. Select Java as the programming language.
3. Create two EditText controls to enter numbers.
4. Create an Add Button.
5. Create an EditText to display the result.
6. Read the two input values.
7. Add the two numbers using Java.
8. Display the sum in the result field.
9. Run and test the application.
10. Upload the project to GitHub.

# XML Code:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="30dp">

    <EditText
        android:id="@+id/number1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="numberDecimal" />

    <EditText
        android:id="@+id/number2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="numberDecimal" />

    <Button
        android:id="@+id/addButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD" />

    <EditText
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Result"
        android:focusable="false"
        android:clickable="false" />

</LinearLayout>


```
# Java Code:
```
package com.example.additionoftwonumbers;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText number1, number2, result;
    Button addButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        number1 = findViewById(R.id.number1);
        number2 = findViewById(R.id.number2);
        result = findViewById(R.id.result);
        addButton = findViewById(R.id.addButton);

        addButton.setOnClickListener(v -> {

            double num1 = Double.parseDouble(number1.getText().toString());
            double num2 = Double.parseDouble(number2.getText().toString());

            double sum = num1 + num2;

            result.setText(String.valueOf(sum));
        });
    }
}


```

# OUTPUT:

<img width="1919" height="1027" alt="Screenshot 2026-09-22 110712" src="https://github.com/user-attachments/assets/e8ac697a-0a3d-46a7-9cf3-18a0bf1beb6f" />




