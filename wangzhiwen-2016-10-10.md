# 2016-10-10工作日志
===================

1.已完成的工作内容

Android Studio布局的学习

2.工作成果

日报登陆系统

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical" android:layout_width="match_parent"
    android:layout_height="match_parent">

    <LinearLayout
        android:background="#00ff00"
        android:layout_width="match_parent"
        android:layout_height="200dp">

        <TextView
            android:text="日报登陆系统"
            android:textSize="50dp"
            android:gravity="center"
            android:layout_width="388dp"
            android:layout_height="86dp" />
    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:text="用户名"
            android:textSize="20dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content">

        </TextView>

        <EditText

            android:layout_width="match_parent"
            android:layout_height="wrap_content" />

    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        <TextView
            android:text="密码"
            android:textSize="20dp"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content">
        </TextView>
        <EditText

            android:layout_width="match_parent"
            android:layout_height="wrap_content" />

    </LinearLayout>

    <LinearLayout
        android:orientation="horizontal"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content">
        <CheckBox
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
        <TextView
            android:textSize="20dp"
            android:text="记住密码"
            android:layout_width="match_parent"
            android:layout_height="wrap_content" />


    </LinearLayout>
    <LinearLayout
        android:orientation="horizontal"
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
            android:layout_height="wrap_content"
            android:id="@+id/button4" />

        <Button
            android:text="忘记密码"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:id="@+id/button3" />
    </LinearLayout>


</LinearLayout>

！[日报登入系统](/pic/)
