# Develop-an-application-that-uses-GUI-components-Font-and-Colors-

Code for Activity_main.xml: 
<?xml version="1.0" encoding="utf-8"?> 
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"     
android:orientation="vertical"     
android:layout_width="match_parent"     
android:layout_height="match_parent"> 
<TextView         
android:id="@+id/textView"         
android:layout_width="match_parent"         
android:layout_height="wrap_content"        
android:layout_margin="30dp"         
android:gravity="center"         
android:text="Hello World!"         
android:textSize="25sp"         
android:textStyle="bold" /> 
<Button         
android:id="@+id/button1"         
android:layout_width="match_parent"         
android:layout_height="wrap_content"         
android:layout_margin="20dp"         
android:gravity="center"         
android:text="Change font size"         
android:textSize="25sp" /> 
<Button         
android:id="@+id/button2"         
android:layout_width="match_parent"         
android:layout_height="wrap_content"         
android:layout_margin="20dp"        
android:gravity="center"         
android:text="Change color"        
android:textSize="25sp" /> 
</LinearLayout>


 Code for MainActivity.java: 
 package com.example.exno1; import android.graphics.Color;  
 import android.os.Bundle; import android.view.View; 
 import android.widget.Button; 
 import android.widget.TextView; 
 import androidx.appcompat.app.AppCompatActivity; 
 public class MainActivity extends AppCompatActivity 
 {     
   int ch=1;     
   float font=30; 
   @Override     
   protected void onCreate(Bundle savedInstanceState)     
   {         
       super.onCreate(savedInstanceState);         
       setContentView(R.layout.activity_main);         
       final TextView t= (TextView) findViewById(R.id.textView);         
       Button b1= (Button) findViewById(R.id.button1);         
       b1.setOnClickListener(new View.OnClickListener() {             
       @Override             
       public void onClick(View v) {                 
       t.setTextSize(font);                 
       font = font + 5;                 
       if (font == 50)                     
       font = 30;             
       }         
       });         
       Button b2= (Button) findViewById(R.id.button2);         
       b2.setOnClickListener(new View.OnClickListener() {             
        @Override             
        public void onClick(View v) {                 
          switch (ch) {                     
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
              if (ch == 7)
              5                      
              ch = 1;             
            }         
        });     
    } 
}

