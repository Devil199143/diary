# 2016-10-19工作日志
===================

1.已完成的工作

使用代码写布局

activity生命周期的理解


2.工作成果

使用代码布局写一个标准计算器

package com.feicui.myapplication;

import android.graphics.Color;
import android.os.Bundle;
import android.support.v7.app.AppCompatActivity;
import android.view.View;
import android.view.ViewGroup;
import android.widget.Button;
import android.widget.EditText;
import android.widget.LinearLayout;
import android.widget.RelativeLayout;
import android.widget.TextView;

/**
 * Created by 王志文 on 2016/10/19.
 */

public class MainActivity extends AppCompatActivity {
    public void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);

        LinearLayout linearLayout=new LinearLayout(this);
        LinearLayout.LayoutParams btParams=new LinearLayout.LayoutParams(ViewGroup.LayoutParams.MATCH_PARENT,
                ViewGroup.LayoutParams.MATCH_PARENT);
        linearLayout.setOrientation(LinearLayout.VERTICAL);

        TextView textView=new TextView(this);
        textView.setBackgroundColor(Color.MAGENTA);
        textView.setHeight(1400);

        linearLayout.addView(textView);

        LinearLayout linearLayout4=new LinearLayout(this);
        LinearLayout.LayoutParams btParams4=new LinearLayout.LayoutParams(ViewGroup.LayoutParams.WRAP_CONTENT,
                ViewGroup.LayoutParams.WRAP_CONTENT);
        linearLayout4.setBackgroundColor(Color.BLUE);

        Button button10=new Button(this);
        button10.setText("AC");
        linearLayout4.addView(button10);
        Button button11=new Button(this);
        button11.setText("0");
        linearLayout4.addView(button11);
        Button button12=new Button(this);
        button12.setText("=");
        linearLayout4.addView(button12);
        Button button_d=new Button(this);
        button_d.setText("/");
        linearLayout4.addView(button_d);

        linearLayout.addView(linearLayout4);

        LinearLayout linearLayout1=new LinearLayout(this);
        LinearLayout.LayoutParams btParams1=new LinearLayout.LayoutParams(ViewGroup.LayoutParams.WRAP_CONTENT,
                ViewGroup.LayoutParams.WRAP_CONTENT);
        linearLayout1.setBackgroundColor(Color.GREEN);

        Button button1=new Button(this);
        button1.setText("1");
        linearLayout1.addView(button1);
        Button button2=new Button(this);
        button2.setText("2");
        linearLayout1.addView(button2);
        Button button3=new Button(this);
        button3.setText("3");
        linearLayout1.addView(button3);
        Button button_a=new Button(this);
        button_a.setText("+");
        linearLayout1.addView(button_a);

        linearLayout.addView(linearLayout1);

        LinearLayout linearLayout2=new LinearLayout(this);
        LinearLayout.LayoutParams btParams2=new LinearLayout.LayoutParams(ViewGroup.LayoutParams.WRAP_CONTENT,
                ViewGroup.LayoutParams.WRAP_CONTENT);
        linearLayout2.setBackgroundColor(Color.RED);

        Button button4=new Button(this);
        button4.setText("4");
        linearLayout2.addView(button4);
        Button button5=new Button(this);
        button5.setText("5");
        linearLayout2.addView(button5);
        Button button6=new Button(this);
        button6.setText("6");
        linearLayout2.addView(button6);
        Button button_b=new Button(this);
        button_b.setText("-");
        linearLayout2.addView(button_b);

        linearLayout.addView(linearLayout2);

        LinearLayout linearLayout3=new LinearLayout(this);
        LinearLayout.LayoutParams btParams3=new LinearLayout.LayoutParams(ViewGroup.LayoutParams.WRAP_CONTENT,
                ViewGroup.LayoutParams.WRAP_CONTENT);
        linearLayout3.setBackgroundColor(Color.YELLOW);

        Button button7=new Button(this);
        button7.setText("7");
        linearLayout3.addView(button7);
        Button button8=new Button(this);
        button8.setText("8");
        linearLayout3.addView(button8);
        Button button9=new Button(this);
        button9.setText("9");
        linearLayout3.addView(button9);
        Button button_c=new Button(this);
        button_c.setText("*");
        linearLayout3.addView(button_c);

        linearLayout.addView(linearLayout3);

        setContentView(linearLayout);
    }
}





3.未完成的工作

无

4.未完成的原因

无

5.遇到的问题及解决方案

请教老师和同学，翻看教材ppt
