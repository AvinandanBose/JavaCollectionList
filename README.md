# JavaNetworking
This is all about Java Networking.

<h1>JavaNetworking </h1>
<h3> The systems connected over a network through the internet connect to each other with the help of Transmission Control Protocol(TCP) or User Datagram Protocol(UDP). In Java, programming is done on the application layer that uses the concept of the classes in the java.net package , which provide networking functions to users. </h3> 



<h1 align="center"> InetAddress[Internet Addressing] </h1>

<ul>
<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetByName%5D.java">GetByName</h3></li>

```Syntax
Determines the IP address of a host, given the host's name.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetAllByName%5D.java">GetAllByName</h3></li>

```Syntax
Given the name of a host, returns an array of its IP addresses, 
based on the configured name service on the system.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetAddress%5D.java">GetAddress</h3></li>

```Syntax
Returns the raw IP address of  InetAddress object. 
As it returns byte value hence we have to do AND
Operation with 0xff(Hex)= 255 (1111 1111), to get actual value.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetHostName%5D.java">GetHostName</h3></li>

```Syntax
Gets the host name for the IP address.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetHostAddress%5D.java">GetHostAddress</h3></li>

```Syntax
Returns the IP address string in textual presentation.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetCanonicalHostName%5D.java">CanonicalHostName</h3></li>

```Syntax
Gets the fully qualified domain name for the IP address.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetLocalHost%5D.java">GetLocalHost</h3></li>

```Syntax
Returns the address of the local host. 
This is achieved by retrieving the name of the host from the system,
then resolving that name into an InetAddress.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BgetLoopbackAddress%5D.java">GetLoopbackAddress</h3></li>

```Syntax
Returns the loopback address.

The InetAddress returned will represent the IPv4 loopback address, 127.0.0.1, 
or the IPv6 loopback address, ::1. 

Note: The IP address 127.0. 0.1 is called a loopback address.
Packets sent to this address never reach the network ,
but are looped through the network interface card only. 
This can be used for diagnostic purposes to verify,
that the internal path through the TCP/IP protocols is working.
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddressTest%5BhashCode%5D.java">HashCode</h3></li>

```Syntax
Returns a hashcode for this IP address.
```


<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddress%5BisAnyLocalAddress%5D.java">isAnyLocalAddress</h3></li>

```Syntax
Utility routine to check if the InetAddress is a wildcard address.
Wild Card Address is a special local IP address.
i.e. 
For Net Mask : 255.255.255.255 → Wild Card Mask : 0.0.0.0
For Net Mask : 255.255.255.254 → Wild Card Mask : 0.0.0.1
For Net Mask : 255.255.255.252 → Wild Card Mask : 0.0.0.3
For Net Mask : 255.255.255.248 → Wild Card Mask : 0.0.0.7
.....

For Net Mask : 0.0.0.0 → Wild Card Mask : 255.255.255.255

Note :

Formula = 
Starting Value is Always : 255.255.255.255
(Substract)
Subnet Mask =  Wild Card Mask

i.e.

255.255.255.255 - Subnet Mask = Wild Card Mask

A wildcard mask is a mask of bits that indicates ,
which parts of an IP address are available for examination.

A wildcard mask can be thought of as an inverted subnet mask.
i.e.
(Subnet Mask)255.255.255.0  → 0.0.0.255(Wild Card Mask)

A wild card mask is a matching rule in which:

0 means that the equivalent bit must match(Care)and 
1 means that the equivalent bit does not matter(Don't Care).
```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddress%5BisLinkLocalAddress%5D.java">isLinkLocalAddress</h3></li>

```Syntax

Utility routine to check if the InetAddress is an link local address.

Linkink Local Address: A link-local address is an automated selected,
IPv6 unicast( one-to-one transmission ) network address ,
that is valid only for communications within the subnetwork that the host is connected to.
A link-local address is required on each physical interface.

Link-local addresses are designed to be used for addressing on a single link,
for purposes such as automatic address configuration, neighbor discovery, 
or in the absence of routers.

It also may be used to communicate with other nodes on the same link. 
A link-local address is automatically assigned.

A link-local address is the IP address that is to be used for communication ,
within a logical division of the network or in the broadcast domain ,
to which the host is connected.

Range of Link Local Ip Address : 169.254.x.x
where x ranges from : 0 - 255 

i.e. The Range is between : 169.254.0.0 -
169.254.255.255

Each computer randomly select an IP address in a given Range.
And then communicate to other Computer searching for the same ,
IP address through ARP(Address Resolution Protocol (ARP)), 
if not found then the automated selected IP belongs to the 
Computer.

Note: A link-local address is an IPv6 unicast address ,
that can be automatically configured on any interface .

```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddress%5BisLoopbackAddress%5D.java">isLinkLocalAddress</h3></li>

```Syntax

Utility routine to check if the InetAddress is a loopback address.

```

<li><h3> <a href="https://github.com/AvinandanBose/JavaNetworking/blob/main/javaInetAddress%5BisMCGlobal%5D.java">isMCGlobal</h3></li>

```Syntax

Utility routine to check if the multicast address has global scope.

Destination Address: It can be Unicast, MultiCast or BroadCast.
  

Multicast: In a Multicast Transmission,
  All stations recieves the frame, the stations that
  are members of the group keeps and handles the frame.
  The protocol that is used  
  Internet Group Management Protocol . 
  It uses Class D of IP address , where 
  1110 - these 4 bits are fixed in Octet
  and other 28 bits can be used in maximum
  of 2^28 bits . Therefore 1st Octet will
  range from : 1110 0000 - 1110 1111
  that is 224-239. And least significant 
  bit of the of the first byte in a destination
  address is always 1 in Multicasting,
  where as in Unicast it is 0.
  
```


</ul>

