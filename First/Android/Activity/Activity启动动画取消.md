代码的方式
```java
Intent intent = new Intent(mContext, MainActivity2.class);
mContext.startActivity(intent);
((Activity) mContext).overridePendingTransition(0, 0);
```

xml的方式

```xml
<!-- Base application theme. -->
<style name="AppTheme" parent="Theme.AppCompat.Light.NoActionBar">
    <!-- Customize your theme here. -->
    <item name="colorPrimary">@color/colorPrimary</item>
    <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
    <item name="colorAccent">@color/colorAccent</item>
    <item name="android:windowAnimationStyle">@style/Animation</item>
</style>

<style name="Animation">
    <item name="android:activityOpenEnterAnimation">@null</item>
    <item name="android:activityOpenExitAnimation">@null</item>
    <item name="android:activityCloseEnterAnimation">@null</item>
    <item name="android:activityCloseExitAnimation">@null</item>
    <item name="android:taskOpenEnterAnimation">@null</item>
    <item name="android:taskOpenExitAnimation">@null</item>
    <item name="android:taskCloseEnterAnimation">@null</item>
    <item name="android:taskCloseExitAnimation">@null</item>
    <item name="android:taskToFrontEnterAnimation">@null</item>
    <item name="android:taskToFrontExitAnimation">@null</item>
    <item name="android:taskToBackEnterAnimation">@null</item>
    <item name="android:taskToBackExitAnimation">@null</item>
    <item name="android:windowEnterAnimation">@null</item>
</style>
```