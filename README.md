# Portfolio-2 Building a Sandboxed Network
# Aims
A sandboxed network provides an essential learning environment and platform, offering a secure, isolated space to simulate real-world network scenarios without introducing risks to live systems. For this Portfolio, you will create your own private sandboxed virtual network using VirtualBox. The network will consist of multiple virtual machines (VMs) configured within a private IP address range. The aim is to gain an applied understanding of networking concepts, IP subnetting, network interface configuration, and a basic server setup, design, planning and organisation strategies.
# Tools
### Ubuntu Desktop 24 :- https://ubuntu.com/desktop
### Ubuntu Server for Getway-Router :- https://ubuntu.com/download/server
### Bitnami :- https://bitnami.com/stacks/virtual-machine

# 1. Ubuntu Desktop 24
### Go to Devices-> Network-> Network Settings-> Adapter 1-> Attached to: Internal Network Name: intent

![image](https://github.com/user-attachments/assets/2700b597-e499-4d89-bc6c-7522f9483413)

### First we want to assign IP address go to the Setting-> Network 

![image](https://github.com/user-attachments/assets/5fc35047-6c94-4849-a360-897ddd85b65b)

### Go to the wired section then click to setting then select IPv4
### In IPv4 Method click to Manual
### Addresses assign Address, Netmask, Gateway

![image](https://github.com/user-attachments/assets/d44a832a-fec5-4227-9b84-6d14fc37cad9)

### Now go to the Terminal then ping the address and getway to see its working or not.
#### command ping 192.168.12.1
#### command ping 192.168.12.2

![image](https://github.com/user-attachments/assets/20db062a-8c4a-4f3c-b15f-81e750658d5e)

# 2. Bitnami
### Go to Devices-> Network-> Network Settings-> Adapter 1-> Attached to: Internal Network Name: intent 

![image](https://github.com/user-attachments/assets/f648e698-0277-47aa-a651-2edb94cc8cc3)

### Assign IP address
#### command sudo nano /etc/network/interfaces

![image](https://github.com/user-attachments/assets/c8991264-f55b-451a-a40b-1b5f36b40a57)

### Ping the address and getway to see its working or not.
#### command ping 192.168.112.1
#### command ping 192.168.112.2
![image](https://github.com/user-attachments/assets/bac236e1-5a74-461c-9461-312cdb3112c9)

# 3. Ubuntu Server for Getway-Router
### Go to Devices-> Network-> Network Settings->

### Adapter 1-> Attached to: NAT

<img width="623" alt="image" src="https://github.com/user-attachments/assets/fe6a8a37-c9e8-4a30-ae48-2cb360d70d9b" />

### Adapter 2-> Attached to: Internal Network Name: intnet

<img width="622" alt="image" src="https://github.com/user-attachments/assets/e34a2df9-da7f-4604-b640-389918d00605" />

### Adapter 3-> Attached to: Internal Network Name: intnet

<img width="622" alt="image" src="https://github.com/user-attachments/assets/b7f67426-e887-4c12-ad54-cd256cdca3e3" />

## Network setting in Getway-Router
#### command sudo nano /etc/netplan/50-cloud-init.yaml

![image](https://github.com/user-attachments/assets/7d598455-9a6d-4f67-81c1-5464bc8eb47f)

### Ping the address and getway to see its working or not.
#### command ping 192.168.12.1
#### command ping 192.168.12.2
#### command ping 192.168.112.1
#### command ping 192.168.112.2

<img width="959" alt="image" src="https://github.com/user-attachments/assets/74ba2626-4af2-47dd-ab4f-add5a55ced0e" />
