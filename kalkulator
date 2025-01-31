package com.example.kalkulator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {

    EditText liczbaA, liczbaB;
    Button nwdLiczby, sumaLiczb, silniaLiczby;
    TextView wynikDzialania;
    int a = 0;
    int b = 0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        liczbaA = findViewById(R.id.liczbaAEditText);
        liczbaB = findViewById(R.id.liczbaBEditText);

        nwdLiczby = findViewById(R.id.buttonNWD);
        sumaLiczb = findViewById(R.id.buttonSuma);
        silniaLiczby = findViewById(R.id.buttonSilnia);

        wynikDzialania = findViewById(R.id.textViewWynik);

        // nwd
        nwdLiczby.setOnClickListener(
                new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        a = Integer.parseInt(liczbaA.getText().toString());
                        b = Integer.parseInt(liczbaB.getText().toString());
                        wynikDzialania.setText(Integer.toString(nwd(a,b)));
                    }
                }
        );

        // suma
        sumaLiczb.setOnClickListener(
                new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        a = Integer.parseInt(liczbaA.getText().toString());
                        b = Integer.parseInt(liczbaB.getText().toString());
                        wynikDzialania.setText(Integer.toString(suma(a,b)));
                    }
                }
        );

        // silnia
        silniaLiczby.setOnClickListener(
                new View.OnClickListener() {
                    @Override
                    public void onClick(View view) {
                        b = Integer.parseInt(liczbaB.getText().toString());
                        wynikDzialania.setText(Integer.toString(silnia(b)));
                    }
                }
        );
    }

    // algorytm NWD z dzieleniem
    private int nwd(int x, int y){
        int r = 0;
        x = Integer.parseInt(liczbaA.getText().toString());
        y = Integer.parseInt(liczbaB.getText().toString());
        while(y!=0){
            r = x%y;
            x = y;
            y = r;
        }
        return x;
    }

    // suma
    private int suma(int l1, int l2){
        return l1+l2;
    }

    // silnia z liczby
    private int silnia(int liczba){
        int silniaLiczby = 1;
        for(int i = 1; i<=liczba; i++){
            silniaLiczby *= i;
        }
        return silniaLiczby;
    }
}
