##  Server

```
from gcm import GCM

gcm = GCM("YOUR_SERVER_KEY")


def send_gcm(db, location, message, gcm_id=None):
    clients = [
        device.gcm_id
        for device in db.query(Device).filter(Device.location == location)
    ] if gcm_id is None and gcm_id == '' else [gcm_id]

    gcm.json_request(registration_ids=clients, data=message)
```
