##  Server cont.

```
class DeviceRegistrationHandler(web.RequestHandler):
    def post(self):

        ...

        gcm_message = {
            'message': "New news item in your location.",
            'timestamp': time.strftime('%Y-%m-%d %H:%M:%S', time.gmtime())
        }

        db.query(News).filter(News.location == location).count() > 0\
            and send_gcm(db, location, gcm_message, gcm_id=device.gcm_id)

```
