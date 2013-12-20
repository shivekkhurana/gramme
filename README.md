gramme
======

A elegant way to pass volatile data around over [UDP (datagrammes)][]
serialized with [msgpack][]

Server
--------------
```
import gramme

@gramme.server(3030)
def my_awsome_data_handler(data):
    print data
```

Client
--------------

```
import gramme

client = gramme.client(host="132.23.x.x", port=3030)

some_data = {'key': 'value'}
client.send(some_data)

more_data = ['i am a list', 1, {'hello': 'there!'}]
client.send(more_data)
```

Installation
------------

Install *gramme* with pip:

    $ pip install gramme

*Note* : This will install [waavwal/gramme](https://github.com/waawal/gramme) package.

---
Todo
----

- Write Tests
- Handle json, string and msgpack gracefully
- Bluetooth support

###Maybe###
- Remove SocketServer Dependency, rely on pure sockets
- Threading
- TCP sockets <-> websockets bridge

---
License
-------

GNU AFFERO GENERAL PUBLIC LICENSE 

Version 3, 19 November 2007

**Required**
- Disclose Source
- License and copyright notice
- State Changes

**Permitted**
- Commercial Use
- Distribution
- Modification
- Private Use

**Forbidden**

 - Hold Liable
 - Sublicensing

[UDP (datagrammes)]: https://en.wikipedia.org/wiki/User_Datagram_Protocol
[msgpack]: http://msgpack.org/