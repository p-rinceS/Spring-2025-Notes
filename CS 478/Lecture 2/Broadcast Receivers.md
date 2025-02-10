

Components that listen for special messages called Intents and respond to those messages.

Intents are broadcast by applications.

Reciever's onRecieve() method specifies actions in response to an intent.


### Example:

Messaging application:
SMS arrives, OS broadcasts intent SMS_RECIEVED.
Broadcast Receiver in messaging app starts service that downloads and stores SMS content locally.

(Reference Slide 38.)