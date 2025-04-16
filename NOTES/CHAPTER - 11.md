
**Secure Network Architecture and Components**

The TCP/IP model was established by DARPA in the year 1970, OSI model was not developed until 1970s.

**OSI MODEL** - Each layer is responsible for performing specific tasks or operations with the ultimate goal of supporting data exchange. 

| **7** | **Application**  |
| ----- | ---------------- |
| **6** | **Presentation** |
| **5** | **Session**      |
| **4** | **Transport**    |
| **3** | **Network**      |
| **2** | **Datalink**     |
| **1** | **Physical**     |

**Encapsulation** - Is the addition of a header and possibly a footer to the data received by each layer from the layer above before its handed off to the layer below. As the message is encapsulated at each layer, the previous layer's header and payload become the payload of the current layer. The inverse action occurring as data moves up through the OSI model layers from physical to application is known as **Deencapsulation**

Total Number of ports 65535

o - 1024 ports are assigned for well known service ports. These are reserved exclusively for servers.

1024 to 49151 - Are known for software ports. These are ports that have one or more networking software products specifically registered for them

49152 to 65535 are known as random, dynamic or ephermeral ports because they are often used randomly and temporarily by clients as a source port. 

The two primary transport layer protocols of TCP/IP are TCP and UDP.

TCP is a full duplex connection, whereas UDP is a simplex connectionless protocol

TCP uses a three way handshake to establish a reliable communication

1. The Client sends a SYN flagged packet to the server.
2. The server responds with a SYN/ACK flagged packet to the client.
3. The client responds with a ACK flagged packet back to the server.

**DISCONNECTING**
1. TCP sends the most common FIN (FINISH) packet to the server to initiate session shutdown
2. Then it uses the RST (reset) flagged packet, which causes an immediate and abrupt session termination 


IPv4 - 32 Bit Addressing
IPv6 - 128 Bit Addressing 

| **CLASS A** | **0** | 1-126 |
| ----------- | ----- | --------- |
| CLASSB      | 10    | 128-191   |
| CLASS C     | 110   | 192-223   |
| CLASS D     | 1110  | 224-239   |
| CLASS E     | 1111  | 240-255   |

Secure Communication Protocols

**IPSEC** - Internet Protocol Security (IPsec) uses public key cryptography to provide encryption, access control, nonrepudiation and message authentication all using IP based protocol. The primary use of IPsec is for virtual private networks (VPN), so IPsec can operation in either transport or tunnel mode. IPsec is a standard of IP security extensions used as an add-on for IPv4 and integrated into IPv6.

**Kerberos** - Kerberos offers a single sign on (SSO) solution for users and provides protection of logon credentials. Modern implementations of Kerberos use hybrid encryption to provide reliable authentication protection. 

**Secure Shell** - SSH is a good example of an end-to-end encryption technique. This security tool can be used to encrypt numerous plaintext utilities (such as rcp,rlogin, and rexec) server as a protocol encrypter such as with SFTP and function as a transport mode VPN 

Network Segmentation 
- Boosting Performance Network
- Reducing Communication Problems
- Providing Security 
These segmentation can be created by using switch-based VLANs routers, or firewalls, individually or in combination. A private LAN or intranet a screened subnet and an extranet are all types of network segments

**SSID** - Service Set Identifier
The SSID is broadcast by the WAP via a special transmission called a beacon frame. A beacon frame allows any wireless NIC within range to see the wireless network and make connecting as simple as possible 

**WEP** - Wired Equivalent Privacy (802.11) 
	WEP uses a predefined shared Rivest Cipher RC4 secret key for both authentication and encryption.

**WPA** - Wi-Fi Protected Access (802.11i) 
	WPA uses separated authentication from encryption also WPA uses the RC4 algorithm and employs the Temporal Key Integrity protocol (TKIP)

**WPA2** - Wi-Fi Protected Access 2 (IEEE 802.11i)
	It implements AWS-CCMP instead of RC4. to date, no attacks have been successful against AWS-CCMP encryption. But there have been exploitations of the WPA2 key exchange processes.  

**AAA service** - 1812 UDP for Radius 
**TACACS+** - TCP 49

**Bridge** - A bridge is used to connect two different networks together, even network of different topologies, cabling types and speeds, Bridges operate at OSI layer 2.

**Switches** -Switches manage the transmission of frames via MAC address. Switches can also create separate broadcast CHAPTERs when used to create VLANs. Switches operate primarily at OSI layer 2, When switches have additional features, such  as routing among VLAN, they can operate at OSI layer 3 as well. 

**Routers** - Routers are used to control traffic flow on networks and are often used to connect similar networks and control traffic flow between the two. Routers manage traffic based on logical IP addressing. They can function using statically defined routing tables, or they can employ a dynamic routing systems. Routers operate at OSI layer 3

**LAN Extenders** - A LAN extender is a remote access, multilayer switch used to connect distant networks over WAN links. Aka WAN switch or WAN router. 

**JumpBox** - A jump server or jump box is a remote access system deployed to make accessing a specific system or network easier or more secure. A jump server is often deployed in extranets, screened subnets or cloud network where a standard direct link or private channels is not available or is not considered safe. 

**Sensor** - A sensor collects information and then transmits it back to a central system for storage and analysis, Sensors are common elements of fog computing, ICS, Iot, IDS/IPS, and SIEM, SOAR. Many sensors are based on SoC. 

**MFD/ UTM/ NGFW** - A firewall with a combination of antivirus scanners, DLP and IDS, plus add on's.

**Baseband** - Can transmit only a single signal at a time and **Broadband** cables can transmit multiple signals simultaneously. Most networking cables are baseband cables. However, when used in specific configurations, coaxial cable can be used as a broadband connection, Such with cable modems.

**Fibre Optic Cable**
- SingleMode
	- 1310nm or 1550nm and can be deployed upto 10KM and its sheathed in yellow
- MultiMode
	-  850nm or 1300nm and has a maximum run length of 400m and sheathed in blue
