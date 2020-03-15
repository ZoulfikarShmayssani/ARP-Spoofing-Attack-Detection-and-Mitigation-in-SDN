
ARP Spoofing mitigation module on POX SDN controller. 

## Features
* Prevent LAN attackers from poisoning cache table entries of nodes with a little overhead.
* Prevent malicious packets from entering network.

## Setup
* ARPspoofperf.py creates the test setup with the detection module.
* ARPspoofperfwithoutsol.py creates the test setup without the detection module. 
* l2_learning_arp_mitigation.py has the ARP mitigation module on POX controller.

### How to Run
* Run the POX controller using 
./pox.py log.level --DEBUG proto.dhcpd --network=10.1.1.0/24 --ip=10.1.1.1 forwarding.l2_learning_arp_mitigation
* Run the topology using
sudo mn --mac --controller remote --topo=single,3
