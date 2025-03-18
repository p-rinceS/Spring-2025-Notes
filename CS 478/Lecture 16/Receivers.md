

You can register receivers statically or programmatically.


##### onReceive dos & don'ts:
Donts: 
- request a dangerous level permision
- bind to a service
- perform network operations


#### Don't spanw a thread:
- Process running receiver may go away after onReceiver() returns