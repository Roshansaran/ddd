# ddd


import android.app.Activity;

import android.graphics.Color;

import android.graphics.Typeface;

import android.os.Bundle;

import android.view.View;

import android.widget.Button; 

import android.widget.TextView;

public class MainActivity extends Activity {

float font = 24;

int i = 1;

@Override

public void onCreate(Bundle savedInstanceState) {

super.onCreate(savedInstanceState);

setContentView(R.layout.activity_main);

final TextView t1 = (TextView) findViewById(R.id.textView1);

Button b1 = (Button) findViewById(R.id.button1);

b1.setOnClickListener(new View.OnClickListener() {

public void onClick(View view) {

t1.setTextSize(font);font = font + 4;

if (font == 40)

font = 20;

}

});

Button b2 = (Button) findViewById(R.id.button2);

b2.setOnClickListener(new View.OnClickListener() {

public void onClick(View view) {

switch (i) {

case 1:

t1.setTextColor(Color.parseColor("#0000FF"));

break;

case 2:

t1.setTextColor(Color.parseColor("#00FF00"));

break;

case 3:

t1.setTextColor(Color.parseColor("#FF0000"));

break;

case 4:

t1.setTextColor(Color.parseColor("#800000"));

break;

}

i++;

if (i == 5)

i = 1;

}

});

final TextView tv = (TextView) findViewById(R.id.textView1);

Button b3 = (Button) findViewById(R.id.button3);

b3.setOnClickListener(new View.OnClickListener() {

public void onClick(View view) {

switch (i) {

case 1:

Typeface type = 

Typeface.createFromAsset(getAssets(),"fonts/SCRIPTBL.TTF"); 

 tv.setTypeface(type);

break;

case 2:

Typeface type1 = 

Typeface.createFromAsset(getAssets(),"fonts/segoesc.ttf"); 

 tv.setTypeface(type1);

break;

}

i++;

if (i == 5)

i = 1;

}

});

}
