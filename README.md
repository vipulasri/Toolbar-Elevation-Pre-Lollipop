## Toolbar Elevation on Pre-lollipop Devices.
As we know Lollipop devices gives us a nice shadow by default, but pre Lollipop doesn’t. <br>Now so to overcome this problem and apply Elevation/Shadow on Pre-lollipop devices.

#### 1. Firstly, we will create a drawable to imitate elevation/shadow 

Create a new XML file `dropshadow.xml` in directory res/drawable

        <?xml version="1.0" encoding="utf-8"?>
        <shape xmlns:android="http://schemas.android.com/apk/res/android" android:shape="rectangle">
            <gradient
                android:startColor="@android:color/transparent"
                android:endColor="#44000000"
                android:angle="90"/>
        </shape>
    
#### 2. We will add the shadow drawable below toolbar

        <LinearLayout 
            xmlns:android="http://schemas.android.com/apk/res/android"
            xmlns:app="http://schemas.android.com/apk/res-auto"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="vertical">

        <android.support.v7.widget.Toolbar
            android:layout_width="match_parent"
            android:layout_height="?attr/actionBarSize"
            android:background="?attr/colorPrimary" />

        <View
            android:layout_width="match_parent"
            android:layout_height="4dp"
            android:background="@drawable/dropshadow" />

        </LinearLayout>


You also can create a another Toolbar in a separate XML file and call it in xml via the `<include/>` tag. 

Ex. `<include layout="@layout/toolbar_shadow" />`


## Result

![Screenshot with shadow](https://github.com/vipulasri/Toolbar-Elevation-Pre-Lollipop/blob/master/screen_with_shadow.png)


