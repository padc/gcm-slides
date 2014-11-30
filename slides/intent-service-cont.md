##  Intent Service cont.

```
    private void sendNotification(String msg) {
        NotificationManager notificationManager = (NotificationManager)
                this.getSystemService(Context.NOTIFICATION_SERVICE);

        PendingIntent contentIntent = PendingIntent.getActivity(this, 0,
                new Intent(this, MainActivity.class), 0);

        NotificationCompat.Builder builder = new NotificationCompat.Builder(this)
                 .setSmallIcon(R.drawable.ic_launcher)
                 .setContentTitle(getString(R.string.msg_new_news))
                 .setStyle(new NotificationCompat.BigTextStyle()
                         .bigText(msg))
                 .setContentText(msg);

        builder.setContentIntent(contentIntent);
        notificationManager.notify(NOTIFICATION_ID, builder.build());
    }
```
