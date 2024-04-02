LLMNR poisoning:

LLMNR poisoning is a man-in-the-middle (MITM) attack that exploits this protocol. An attacker sends out a fake LLMNR response pretending to be from the computer with which the name was requested.


LLMNR stands for Link-Local Multicast Name Resolution and is used by Windows to resolve the names of neighbouring computers without using a domain name system (DNS) server. LLMNR works by sending out multicast queries over local networks asking if any specific computers with certain names exist and whether any have responded with their IP addresses when queried by LLMNR.


Goal :We want to use LLMNR poisoning and get domain administrator and system user access.
