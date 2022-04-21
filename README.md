# TRTP_binaries
Binaries to test interoperability\
Compiled on Linux UDS (Ubuntu)\
If you need another compilation please ask in issues\
If you have any problems with run, or any error like segfault please notice us in issues too.

All arguments of the command below can be changed

### Start receiver
```
./receiver -s stats_rec.csv :: 8088 1>file  2>receiver.log
```
-*::* can be replaced by an ipv6 or a domain name (:: listen all address until one is communicating) \
-*8088* is the port listen and used to transmit packet (ACK)\
-*stats_rec.csv* is the file where receiver stats are saved (with -s argument) \
-*receiver.log* is the file where stderr is saved \
-*file* is the file you received


### Start sender
```
./sender -s stats_send.csv ::1 8088 2>sender.log < file
```
-*::1* can be replaced by an ipv6 or a domain name \
-*8088* is the port used to transmit packet \
-*stats_send.csv* is the file where sender stats are saved (with -s argument) \
-*sender.log* is the file where stderr is saved \
-*file* is the file you want to transfer
