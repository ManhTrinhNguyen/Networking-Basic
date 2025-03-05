# Networking-Basic

## How Data Flow through the Internet 

### Network Devices

#### Host 

```
  - Hosts are any device which send and recivece traffic : Computer, Phone, Printer, Cloud Server ...

  - Also the Internet of Things devices : TV, Speaker, Smart Watch, Lights , ....
```

**2 Categories of Host**

```
  - Client and Server

  - Clients are initial the Request . Server are Respone the request

  - A Server is a Computer with software installed which know how to Response the Request 
```

#### IP Address 

```
  - IP Address are the Identify of each Host

  - Each Host must have the IP Address to send and recieve Package on Network

  - When sending the Package from Client to Server . Client will stamped the Source IP Address and Destination IP Address .

  - Source IP Address is Client IP Address

  - Destination IP Address is Server IP Address 
```

#### Network 

<img width="600" alt="Screenshot 2025-03-05 at 12 54 19" src="https://github.com/user-attachments/assets/73c86345-913f-4d5b-88a6-3acb1edeb6cb" />

```
  - Network does the transportation traffic between Hosts

  - Network allow 2 Computer share Data Automatic

  - Network is Logical Grouping of Hosts require similar connectivity

  - Anytime 2 hosts connected . I have Network

  - Network can contain other Network . Subnets or Sub-network . I can have Network within Network within Network ...

  - If I want Network from Tokyo to connect with Network in London . I can't connect it directly . Instead all those network will connect to central Resources namely the Internet

  - Internet is a bunch of intertconnected networks .
```

#### Switch 

<img width="700" alt="Screenshot 2025-03-05 at 13 15 44" src="https://github.com/user-attachments/assets/3ed32b19-c0f8-4978-8487-0daf99167dde" />

```
  - Switch are networking devices facilitate communication within a Network

  - Switch can learn which Host are connected to each Port

  - All the devices connected by Switch within LAN are belong to the same Network . Moreover Networks all share the same IP Address space 
  
```


#### Router 

```
  - Router facilitate communication between Network

  - At the very least I am going to need the Router to connect me with the ultimate network of network known as the Internet

  - Router provide traffic control point between Network (Security, Filtering, redicrecting)

  - Since Router sit on the boundary between Network they provide the logical Localtion to apply security Policies

  - The Network boundary meant to be the logical separation devices

  - The way Router work is that they Learn which nerwork they are attached to . Meaning this Rourer is going to learn that on this Network 

  - A Routers has a IP Address in every Network that they are attached to . This IP Address of the Router known as Gateway

  - Step higher . Router is what create the hierarchy in Network and IP address .

  - The Internet is nothing more is a bunch of Router itself 
```

**Routing Table**

```
  - Routing Table is a database inside the Router that store infomations about paths to different Network . I help Router determine best route to forward packet

  - Path to a Network is Route 
```

**Important Note**

```
  - Routing is a process of moving data between network
  - Router is a device to perform the primary purpose of Routing

  - Switching is a process o moving data within network
  - Swtich is a device to perform the primary purpost of Switching

  - There are many type of Network Devices :

    - Access Points
    - Firewall
    - Loadbalancer
    - Layer 3 Swtich
    - IDS/IPS
    - Proxis
    - Virtual Switches, Virtual Router

  - All of them perform Routing or Switching or Both
```






