## SlideBottomLayout-Android

[![](https://jitpack.io/v/qingmei2/SlideBottomLayout-Android.svg)](https://jitpack.io/#qingmei2/SlideBottomLayout-Android)

## Android底部上拉控件

![usage](https://github.com/qingmei2/SlideBottomLayout-Android/blob/master/pictures/usage.gif)

### If you have a problem (using a problem, or encounter a bug), welcome to provide your issues! Thank you for using SlideBottomLayout-Android!

## <h2 id="Usage">Usage</h2>
### 1. Add code into your Project Build.gradle:
```
allprojects {
  repositories {
    ...
    maven { url 'https://jitpack.io' }
  }
}
```
### 2.Add code into your Module Build.gradle:
```
dependencies {
     compile 'com.github.qingmei2:SlideBottomLayout-Android:1.1'
}
```
### 3.Add view in your layout:

> Warning：this Layout just can hold one child-View like the ScrollView, so you need create a viewGroup to organize other views

```
    <com.qingmei2.library.SlideBottomLayout
        android:id="@+id/slideLayout"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_marginTop="200dp"
        app:handler_height="50dp">
        
        <!--app:handler_height:the height that will show on the screen-->
        <!--Just one child-->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">

            <TextView
                android:id="@+id/handle"
                android:layout_width="match_parent"
                android:layout_height="50dp"
                android:background="#d95858"
                android:gravity="center"
                android:text="handle"
                android:textColor="@android:color/white"
                android:textSize="16sp" />

            <android.support.v7.widget.RecyclerView
                android:id="@+id/recycler_view"
                android:layout_width="match_parent"
                android:layout_height="wrap_content">

            </android.support.v7.widget.RecyclerView>

        </LinearLayout>

    </com.qingmei2.library.SlideBottomLayout>
```

## API(Please reading the Sample code)

| Method                                                                    |detail                  |return |
| -------------                                                           | -------------             | -----|
| show()                         | show this view  | Void |
| hide()                                        | hide this view    | Void  |
| arriveTop()| whether the view is arrive the top | Boolean |
| switchVisible()                                        |switch this view's state (show or hide)      | Void|
| setVisibilityHeight(float visibilityHeight)            |the controlSlideBottomLayout automatically switches the threshold of the state | Void|
| setHideWeight(float hideWeight)                        |the childView Initially visible height      | Void|