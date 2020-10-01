mptcp-ns3
1. INTRODUCTION
Nowadays mobile equipment have often more than one
single network interface. For instance, laptops have usually
at least both a wired (Ethernet) and a wireless (Wifi) network adapters. Similarly smartphones and tablet PCs can
reach the Internet either through Wifi or through a cellular
network (UMTS or 3G+).
Another fact is that network operators usually duplicate
links and equipments in order to protect their networks
against failures, especially in the access and the backhaul
networks. Moreover the backbone networks are generally
meshed. In this context many paths may exist between any
two endpoints. The idea to use concurrently many paths has
then emerged, to improve the robustness and performance of
end-to-end connections. Such multipath connections can indeed balance the load between the different paths, switching
dynamically and automatically the traffic from congested,
disrupted or broken links to the best paths.
A lot of studies have considered the implementation of
multipath capabilities at different layers: at the application
layer [5], at the transport layer [13], [6], [1], [17], [20], [16],
[6], etc. Following these last references, and [19], we think
that the transport layer is a good place to implement multipath capabilities.
At this layer, end-systems can gather information about
each used path: capacity, latency, congestion state. These
information can then be used to react to congestion events
in the network by moving the traffic away from congested
paths. An IETF’s working group has recently been created
to specify a multipath protocol at the transport layer Multipath TCP [3] (MPTCP). More precisely, this working group
develop protocol extensions to Transmission Control Protocol (TCP), the most used transport protocol on Internet,
to handle multiple sub-connections following different paths
between two endpoints.
Previous works in simulating MPTCP [7] focused on congestion control mechanisms without implementing other parts
of MPTCP. This restriction was inherited from the used
simulator, which does not allow the creation of an accurate
model of the simulated protocol. Our contribution consists
of the proposal of a model of MPCTP with a better fidelity,
and also the proposal of enhancing the current version of
MPTCP with packet reordering mechanisms to cope with
the variety of path characteristics.
