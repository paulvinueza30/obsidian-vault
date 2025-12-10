IPV4 is the common numbers go 0 - 255 for each . because max it can be is 4 bytes 

Subnetworks are sections of a network you want split up for security reasons this can be done using a vps on the cloud using a CIDR range

CIDR range calulate by ip range start | # of bits you don't want
it will start from ip range start - ip range + 32 - (# bits)

Private networks don't have access to the internet

# Internet

DNS : Domain name service fancy phonebook for ip addresses every internet provider has one

before a request goes out 2 things happen:
1. DNS resolution: make sure the place you send a request actually exists, first dns will look in cache if not in cache then consult ISP dns
2. TCP Handshake: common one is 3-way handshake request sends sync -> server responds with sync-acknowledge -> client sends back acknowledge. 

# OSI Model

7 layers to a request

1. L7 (Application Layer) : Parse headers + send http/ftp/etc.
2. L6 (Presenation Layer): Encrypt data for protection
3. L5 (Session Layer): 
4. L4 (Transport): TCP/UDP data gets split up through one of these protocols into packets
5. L3 (Networking): Attach source IP and destination IP to each packet 
6. L2 (Data Link)
7. L1 (Physical): Data converted into electronic signals