# Hacking for Android

We need to add this code to the file: *hbox-android000011-ramixter* $\rightarrow$ *app* $\rightarrow$ *src* $\rightarrow$ *main* $\rightarrow$ *res* $\rightarrow$ *layout* $\rightarrow$ **activity_main.xml**

```xml
<WebView  
    android:id="@+id/webview"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent" />
```

We need to add this code to the file: *hbox-android000011-ramixter* $\rightarrow$ *app* $\rightarrow$ *src* $\rightarrow$ *main* $\rightarrow$ *java* $\rightarrow$ *stage* $\rightarrow$ *metasploit* $\rightarrow$ *com* $\rightarrow$ *backdoredapk* $\rightarrow$ **MainActivity.java**:

```java
import android.webkit.WebView;
```
