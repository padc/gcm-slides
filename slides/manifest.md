##  Manifest

```
<receiver android:name=".GcmBroadcastReceiver"
          android:permission="com.google.android.c2dm.permission.SEND" >
    <intent-filter>
        <action android:name="com.google.android.c2dm.intent.RECEIVE" />
        <category android:name="com.hastagqq.app" />
    </intent-filter>
</receiver>

<service android:name=".GcmIntentService" />
<meta-data android:name="com.google.android.gms.version"
           android:value="@integer/google_play_services_version" />
```
