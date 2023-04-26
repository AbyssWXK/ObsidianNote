光标样式
```xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="rectangle">
    <size android:width="1dp" />
    <solid android:color="#4A90E2" />
</shape>
```
view设置
```xml
<EditText
                android:id="@+id/ed_pwd"
         		android:textCursorDrawable="@drawable/cursor_style"
                android:textColor="#000"
                android:textSize="@dimen/sp_24"
                android:paddingLeft="@dimen/dp_15"
                android:layout_width="wrap_content"
                android:layout_height="@dimen/dp_65"/>
```