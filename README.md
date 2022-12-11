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

</ul>

