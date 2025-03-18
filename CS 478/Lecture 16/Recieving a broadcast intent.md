


Broadcast receiver defines method **onReceive(context, intent)**

context = context in which receiver is running
intent = intent sent by [[Broadcast Receivers]]


App A can send a broadcast with a specific action to which App B's receiver is listening, and App B's receiver can then take appropriate action upon receiving the broadcast.

(We used this paradigm in our Battleship method when we broadcasted )