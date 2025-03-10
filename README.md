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

### OSI Models

```
  - The rules of Networking divide into 7 Layers

  - Each layer serves a specific function

  - If all layers are functioning . Hosts can share data
```

**Layer 1: Physical Layer**

```
  - Computer Data exist in form of Bits (1's and 0's)

  - The goal of Physical Layer is Transporting Bits

  - Anything that contribute moving ones and zeros from this computer to this computer is consider a layer one technology

  - For example : Cable, Wire, Wi-fi... 

```

**Layer 2 : Data Link | Hop to Hop**

<img width="700" alt="Screenshot 2025-03-05 at 14 01 04" src="https://github.com/user-attachments/assets/984ee4cc-6e10-4e6a-9a31-c367527a2e7a" />

```
  - Layer 2 is going to interact with Wire (Layer one) . Going to put bits on the Wire and retrive bits from wire

  - Which mean whatever this wire actually connects on the Computer is consider the layer 2 item : NIC (Network Interface Card) / Wifi Access Card

  - The overall goal of layer 2 is what I am going to call Hop to Hop delivery .

  - Meaning Layer 2 Exist to take 1's and 0's from this NIC and move it to other NIC . To Accomplish this goal layer 2 is going to use a specific Addressing Scheme

  - Addressing Scheme : is known as MAC Address

  - MAC Address is 48 bits which are represented as 12 hex digits . MAC Address allow data to go from 1 NIC to the next NIC

  - Every single NIC has a unique MAC Address

  - Switches also exist at Level 2 .

  - Swtiches are devices that facilitate communication within network meaning if these 2 hosts are connected via this Switch . Switch is going to help traffic move along to accomplish this Hop . Moreover Switches allow many devices connected to them

  - Generally with the Internet I am communicating with things that are far away so it is very common for communication between hosts to require multiple hops . Meaning we need to jump accross multiple Router to get to the target Host . Each of those Router are connected to a wire using a NIC and therefore each of those NIC has its own MAC Address . And Layer 2 will handle taking data from First Mac Address and deliver it to next MAC Address then from NIC to NIC

  - If Layer 2 is taking care of eveything Hop . What is taking care of ensuring data goes from this endpoint to the next . So that Layer 3 come in to play
```

**Layer 3: Network**

```
  - Layer 3 goal is call End to End delivery

  - Layer 3 Addressing Scheme : IP Address

  - Every hosts will be identify by its IP Address . These IP Address allow data go from A to B

  - Layer 3 technology : Router, Host (Anything with IP)

  ----How packets flow through the Internet----

  - Let say Host A has DATA want to send to Host B - That DATA is a bunch of 1's and 0's Layer 2 and 3 don't know what they contain

  - Since Host A know that DATA is going to send to Host B . Host A will add Layer 3 infomation to that data

  - Layer 3 Infomation is contain : Source IP Address and Destination IP Address . In order to get that Data from one end to another

  - But the First Step will be getting that Data to the First Router so Host A will add infomation of Layer 2 to that Data

  - Layer 2 Infomation containe : Source MAC Address of Host A NIC and Destination MAC Address of the Frist Router NIC . Once data get there it will remove Layer 2 Infomation . From this point First Router knows data need to move to the Next Router , to do this Data will add another Layer 2 . so on and so on ...

  - Until Data reach Host B . It will also remove Layer 3


  - There is a ARP - Address Resolution Protocol tie Layer 2 and 3 together 
```

**Layer 4 : Transport | Service to Service**

<img width="700" alt="Screenshot 2025-03-05 at 14 54 06" src="https://github.com/user-attachments/assets/c2fab24e-dcdf-4202-b943-a60df60e0609" />

```
  - The overall goal of Layer 4 is Service to Service Delivery

  - Let say I have 1 computer that run multiple Software at the same time . Each of those program meant to send and recived data on the Wire

  - All of those Data will be destined to this Layer 3 Header to accomplish End to End delivery . and Layer 2 Header to accomplish Hop to Hop delivery . How do I make sure the right Program Reivce the right Packets ?

  - Layer 4 is there to distingush Data Stream . It will take all the incoming data and make sure the Right Program get the Right Data

  - Layer 4 Addressing Scheme : Ports .

  - There are 2 set of PORTS : 0-65535 TCP, 0-65535 UDP

  - TCP and UDP is 2 different Strategy to distingush Data Stream . TCP favor reliable , UDP favor efficency

  - Every single program that is expected to recivece or send data on the Wire is going to associated with a particular PORT Number then when data arrives on the Wires it's going to include the Layer 4 Header in addition Layer 2 and 3

  - That Layer 4 Header will indicate which particular program should be reciving the data that what's Layer 4 going to use to make sure the right program recivec the righ 1's and 0's
```

**More Detail Layer 4**

```
  - Server is noting more is a Computer has software installed that know how to response the Specific Request .

  - Server listen for request to pre-defined Ports

  - When a client is making a request to these Server it is not only making a request to this IP Address it is also make a request to a specific PORT

  - Then Each request make by Client . The Client is going to choose a random port Number to use as a source PORT for Connection

  - So the Connection from Client to Server will container : Source IP address , Source PORT and Destination IP Address and Destination PORT .

```
















