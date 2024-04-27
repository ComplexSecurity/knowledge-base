A reverse proxy does the exact opposite of what a [forward proxy](../terms/proxy.md) does. While a forward proxy proxies on behalf of clients (or requesting hosts), a reverse proxy proxies on behalf of servers. A reverse proxy accepts requests from external clients on behalf of servers stationed behind it as shown below.

![reverse_proxy-resized-600-21](https://www.jscape.com/hs-fs/hubfs/social-suggested-images/reverse_proxy-resized-600-21.png?width=600&name=reverse_proxy-resized-600-21.png)

In the example above, the reverse proxy is providing file transfer services. The client is oblivious to the file transfer servers behind the proxy, which are actually providing those services. In effect, where a forward proxy hides the identities of clients, a reverse proxy hides the identities of servers.

An Internet-based attacker would find it considerably more difficult to acquire data found in those file transfer servers than if he didn't have to deal with a reverse proxy.

Just like forward proxy servers, reverse proxies also provide a single point of access and control. You typically set it up to work alongside one or two firewalls to control traffic and requests directed to your internal servers.

In most cases, reverse proxy servers also act as load balancers for the servers behind them. Load balancers play a crucial role in providing high availability to network services that receive large volumes of requests. When a reverse proxy performs load balancing, it distributes incoming requests to a cluster of servers, all providing the same kind of service. 

Both types of proxy servers relay requests and responses between clients and destination machines. But in the case of reverse proxy servers, client requests that go through them normally originate over [TCP/IP](../networking/tcpip.md) connections, while, in the case of forward proxies, client requests normally come from the internal network behind them.