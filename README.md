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

```java
setContentView(R.layout.activity_main);
        WebView webView = (WebView) findViewById(R.id.webview);
        webView.getSettings().setJavaScriptEnabled(true);
        webView.loadUrl("<MY_LINK>");
```

and we will have to replace <MY_LINK> with the link we want to which the application redirects us, for example: https://www.facebook.com/, https://www.youtube.com/, https://www.google.com/, etc.
