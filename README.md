# Add Picasso lib for download images

in file 'build.gradle'
```java
dependencies {
       ...
       implementation ''com.squareup.picasso:picasso:2.5.2''
       ...
    }
```
Sync The Project Create one imageview in Layout
```java
<ImageView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:id="@+id/imageView"
    android:layout_alignParentTop="true"
    android:layout_centerHorizontal="true">
</ImageView>
```
Add the Internet permission in Manifest file
```java
<uses-permission android:name="android.permission.INTERNET" />

//Initialize ImageView

ImageView imageView = (ImageView) findViewById(R.id.imageView);

//Loading image from below url into imageView

Picasso.get()
   .load("YOUR IMAGE URL HERE")
   .into(imageView);

```
