Here's the cleaned-up version of the code without line numbers:

```java
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
    Button button0, button1, button2, button3, button4, button5, button6,
           button7, button8, button9, buttonadd, buttonSub, buttonDiv,
           buttonMul, buttonPoint, buttonReset, buttonEqual;
    EditText eT;
    float ValueOne, ValueTwo, result;
    boolean Addition, Subtract, Multiplication, Division;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        // Referencing
        button0 = (Button) findViewById(R.id.btnZero);
        button1 = (Button) findViewById(R.id.btnOne);
        button2 = (Button) findViewById(R.id.btnTwo);
        button3 = (Button) findViewById(R.id.btnThree);
        button4 = (Button) findViewById(R.id.btnFour);
        button5 = (Button) findViewById(R.id.btnFive);
        button6 = (Button) findViewById(R.id.btnSix);
        button7 = (Button) findViewById(R.id.btnSeven);
        button8 = (Button) findViewById(R.id.btnEight);
        button9 = (Button) findViewById(R.id.btnNine);
        buttonPoint = (Button) findViewById(R.id.btnPoint);
        buttonadd = (Button) findViewById(R.id.btnadd);
        buttonSub = (Button) findViewById(R.id.btnSub);
        buttonMul = (Button) findViewById(R.id.btnMul);
        buttonDiv = (Button) findViewById(R.id.btnDiv);
        buttonReset = (Button) findViewById(R.id.btnReset);
        buttonEqual = (Button) findViewById(R.id.btnEqual);

        eT = (EditText) findViewById(R.id.eT);

        // Event Listeners
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "1");
            }
        });
        button2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "2");
            }
        });

        button3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "3");
            }
        });

        button4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "4");
            }
        });

        button5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "5");
            }
        });

        button6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "6");
            }
        });

        button7.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "7");
            }
        });

        button8.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "8");
            }
        });

        button9.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "9");
            }
        });

        button0.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + "0");
            }
        });

        buttonReset.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText("");
            }
        });

        buttonPoint.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                eT.setText(eT.getText() + ".");
            }
        });

        buttonadd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                ValueOne = Float.parseFloat(eT.getText().toString());
                Addition = true;
                eT.setText(null);
            }
        });

        buttonSub.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                ValueOne = Float.parseFloat(eT.getText().toString());
                Subtract = true;
                eT.setText(null);
            }
        });

        buttonMul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                ValueOne = Float.parseFloat(eT.getText().toString());
                Multiplication = true;
                eT.setText(null);
            }
        });

        buttonDiv.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                ValueOne = Float.parseFloat(eT.getText().toString());
                Division = true;
                eT.setText(null);
            }
        });

        buttonEqual.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                ValueTwo = Float.parseFloat(eT.getText().toString());

                if (Addition == true) {
                    result = ValueOne + ValueTwo;
                    eT.setText(String.valueOf(result));
                    Addition = false;
                }

                if (Subtract == true) {
                    result = ValueOne - ValueTwo;
                    eT.setText(String.valueOf(result));
                    Subtract = false;
                }

                if (Multiplication == true) {
                    result = ValueOne * ValueTwo;
                    eT.setText(String.valueOf(result));
                    Multiplication = false;
                }

                if (Division == true) {
                    result = ValueOne / ValueTwo;
                    eT.setText(String.valueOf(result));
                    Division = false;
                }
            }
        });
    }
}
```
