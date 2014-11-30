##  Intent Service

```
public class GcmIntentService extends IntentService {
    private static final String TAG = GcmIntentService.class.getSimpleName();

    public static final int NOTIFICATION_ID = 1;

    public GcmIntentService() {
        super(Constants.SENDER_ID);
    }

    @Override
    protected void onHandleIntent(Intent intent) {
        Bundle extras = intent.getExtras();
        GoogleCloudMessaging gcm = GoogleCloudMessaging.getInstance(this);
        String messageType = gcm.getMessageType(intent);

        if (extras != null && !extras.isEmpty()) {
            if (GoogleCloudMessaging.MESSAGE_TYPE_MESSAGE.equals(messageType)) {
                sendNotification(getString(R.string.msg_view_news));
            }
        }

        GcmBroadcastReceiver.completeWakefulIntent(intent);
    }

    ...
}
```
