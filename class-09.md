# WRRC and Java

## The HTTP Request Lifecycle
The applications consist of mainly two parts: server and client. When the developer implement an application, there is a connection between servers should be implemented to enable the user doing some searches. The user will send a ***HTTP REquest*** so, host, and optional port number, resource path, and query strings that are specified in the form ***<protocol>://<host><:optional port>/<path/to/resource><?query>.***
This request will be send as a query with all of the information that server needs to reply to that request(query). The browser need to resolve an IP address, then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, user's router’s cache, and user's DNS cache.
* Resolving an IP from a DNS server: is a sequence that includes many steps, and includes fail overs if the first request fails to return an address.

### The Request Journey
1. Local Processing 
If the cache lookup fails, the browser fires off a DNS request using UDP3.
The DNS request contains the preconfigured IP for user's DNS server and user's return IP in its header. 
* ***UDP*** is a lightweight protocol, but the tradeoff is that it offers no guarantees in terms of delivery, and there is no acknowledgement other than a response being sent and received.
The request travels many network devices to reach the target DNS server as packets and whenever the packet hits a piece of networking equipment, the device uses a routing table to determine which other device it is connected to that is most likely situated along the shortest path to the destination. Once the request arrives at user's configured DNS server, the server looks for the address associated with the requested hostname. If it finds one, it sends a response. If an address for the given domain cannot be resolved, the server responds with a failure and your browser returns an error.If the response makes it back the requesting client now has a target IP. 
It will also have received a piece of information as part of the answer that will let it know how long the returned answer can be cached for.


2. Establish a TCP Connection
The client has an IP address,so it can send an HTTP5 request, but first, the client must open a TCP connection because the request is sent over TCP6, which is a transport layer protocol like UDP.
The sequence number allows the receiver to re-order received packets back into their original order, and allows the sender to retransmit any packet that does not get acknowledged by the receiver.
The server must already be "listening" on a port, performing a passive open, after which the client can initiate an active open, and the handshake works as follows:
1. The client initiates the active open by sending a SYN control packet to the server.
2. The server responds with a SYN-ACK message, which contains an acknowledgement number for the original message.
3. The client sends an ACK message back to the server with a sequence number that should match the SYN-ACK message’s acknowledgment number.

After this journey, the request will has a reply, that is called response, that hold either the information that the user send a query request to get or a message that tell the user that the query is failed to find what he/she are searching about.
