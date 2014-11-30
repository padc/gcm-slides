##  Architecture

* Server sends message to GCM server
* GCM queues message
* GCM sends message if device is online
* Android receives message and sends a broadcast
* App wakes up
* App processes the message
