# 2016-10-11工作日志
===================

1.已完成的工作内容

Android Studio布局的学习

2.工作成果

<RelativeLayout
        android:id="@+id/a1"
        android:background="#00ffff"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentTop="true"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true">
        <EditText
            android:text="登陆界面"
            android:textColor="#ff00ff"
            android:textSize="50dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:id="@+id/editText"
            android:layout_alignParentTop="true"
            android:layout_centerHorizontal="true" />
    </RelativeLayout>

    <RelativeLayout
        android:id="@+id/a2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/a1"
        android:layout_alignParentLeft="true"
        android:layout_alignParentStart="true">

        <EditText
            android:id="@+id/b2"
            android:layout_toRightOf="@id/b1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_alignBottom="@+id/b1" />
        <TextView
            android:id="@+id/b3"
            android:layout_below="@+id/b1"
            android:text="密码："
            android:textSize="30dp"
            android:layout_alignRight="@id/b1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
        <EditText
            android:id="@+id/b4"
            android:layout_toRightOf="@id/b3"
            android:layout_below="@id/b1"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_alignBottom="@+id/b3" />
        <CheckBox
            android:id="@+id/b5"
            android:layout_below="@id/b3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
        <TextView
            android:id="@+id/b6"
            android:layout_toRightOf="@id/b5"
            android:layout_below="@id/b3"
            android:layout_alignBottom="@id/b5"
            android:text="记住密码"
            android:textSize="25dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
        <TextView
            android:id="@+id/b7"
            android:text="忘记密码"
            android:textSize="25dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignBottom="@+id/b6"
            android:layout_alignParentRight="true"
            android:layout_alignParentEnd="true" />

        <TextView
            android:id="@+id/b1"
            android:text="用户名："
            android:textSize="30dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
    </RelativeLayout>
    <LinearLayout
        android:id="@+id/a3"
        android:layout_below="@id/a2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        <Button
            android:text="登陆"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
        <Button
            android:text="注册"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
    </LinearLayout>
</RelativeLayout>

3.未完成的工作

无

4.未完成的原因

无

5.遇到的问题及解决方案

请教老师及同学
