`tracert` - lists all the routers between two systems. In this context, each router is referred to as a hop.

Windows uses `tracert` while Linux uses `traceroute`, but they function similarly.

Network admins use `tracert` to identify faulty routers on the network. Ping tells them if they can reach a distant server. If the ping fails, they can use `tracert` to identify where the traffic ends, some hops will succeed, but somewhere `tracert` will identify where packets are lost, giving insight into where the problem occurred.
Other times, they will see where the round-trip times (RTT) increase as traffic is routed around a faulty router.

`tracert` from a security perspective can be used to identify modified paths such as an attacker installing a router between an existing router and the internet.

`tracert -d [hostname]` - combines `ping` and `tracert` commands. After identifying the hops, it pings each hop and computes statistics based on how many pings were sent and how many were received in response.

Admins commonly use it to locate potential problems in the path between two systems. Often an effective method of locating intermittent problems on any hops or problems on any of the segments between two hops.
`Pathping` first displays the hops the same way `tracert` does, numbering each hop.
By default, it tests each hop for 25 seconds, so the total time it takes to finish varies depending on how many routers are in the path.
