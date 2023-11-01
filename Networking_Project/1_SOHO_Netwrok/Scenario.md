# Project : Small Office Home Office Network SOHO 

## Project case Study and Requirements : 

XYZ company is a fast-growing company in Eastern Australia with more than 2 million customers globally. The company deals with selling and buying of food items, which are basically operated from the headquarters. The company is intending to open a branch near the local village Bonalbo. Thus, the company requires young IT graduates to design the network for the branch. The network is intended to operate separately from the HQ network. Being a small network, the company has the following requirements during implementation;
  - One router and one switch to be used (all CISCO products).
  - 3 departments (Admin/IT, Finance/HR and Customer service/Reception).
  - Each department is required to be in different VIANS.
  - Each department is required to have a wireless network for the users.
  - Host devices in the network are required to obtain IPv4 address automatically.
  - Devices in all the departments are required to communicate with each other.


Assume the ISP gave out a base network of 192.168.1.0, you as the young network engineer who has been hired, design and implement a network considering the above requirements.

### Technologies Implemented
  1. Creating a Simple Network using a Router and Access Layer Switch.
  2. Connecting Networking devices with Correct cabling.
  3. Creating VLANs and assigning ports VLAN numbers.
  4. Subnetting and IP Addressing.
  5. Configuring Inter-VLAN Routing (Router on a stick).
  6. Configuring DHCP Server (Router as the DHCP Server).
  7. Configuring WLAN or wireless network (Cisco Access Point).
  8. Host Device Configurations.
  9. Test and Verifying Network Communication.



### Subnetting

Host : 192.168.1.0


We need 3 networks : 
- Admin IT 20  
- Finance/HR 40 
- Customer Service Reception 120 





Lets start with Admin IT 
Host : 192.168.1.0 / 24 
We need 20 host 
2 ^ 5 = 32
32 - 2 = 30 
32 - 5 = 27
<br>


Host + Mask :192.168.1.0 / 27 
The mask : 255.255.255.224
hosts range : 192.168.1.1 - 192.168.1.30
Gateway : 192.168.1.1 
Brodcast : 192.168.1.30 

<br>



- Finance / HR : 
Host : 192.168.1.0 / 24 

we need 40 host 

2 ^ 6 = 64 
64 - 2 = 62 
62 > 40 

so 

32 - 6 = 26

the host  + mask : 192.168.1.0/26
mask : 255.255.255.192
host range : 192.168.1.1 - 192.168.1.62
Gateway : 192.168.1.1   
Brodcast : 192.168.1.62  


<br>

- Customers Service/Reception

We need  120 hosts 

2 ^ 7 = 128 
128 - 2 = 126 
126 > 120 

32 - 7 = 25 
Net + Musk = 192.168.1.0 / 25 
musk : 255.255.255.128
hosts range : 192.168.1.1 - 192.168.1.126
Gateway : 192.168.1.1 
Brodcast : 192.168.1.126


<br>

