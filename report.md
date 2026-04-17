# Summary

In this experiment, a learning switch was implemented using Software Defined Networking (SDN) with a POX controller and Mininet. The controller dynamically learned MAC addresses by observing incoming packets and maintained a MAC-to-port mapping. Based on this information, it installed forwarding rules in the switch, enabling efficient packet delivery without unnecessary flooding.

Initially, when the destination MAC address was unknown, packets were flooded to all ports. Once the controller learned the MAC addresses, it installed flow rules in the switch, allowing packets to be forwarded directly to the correct port. This behavior demonstrates the working of a learning switch in an SDN environment.

---

# Results

* Successful communication between all hosts was achieved with 0% packet loss
* MAC address learning was verified through reduced latency in subsequent pings
* Dynamic flow rule installation was confirmed using flow table inspection
* The switch forwarded packets efficiently after learning, avoiding flooding

---

# Conclusion

The learning switch was successfully implemented and validated. The controller effectively learned MAC addresses and installed forwarding rules, improving network performance and efficiency.
