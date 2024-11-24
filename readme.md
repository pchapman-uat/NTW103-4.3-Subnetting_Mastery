# Assignment 4.3: Subnetting Mastery


1. What are the seven elements of a subnetting question, and what do they mean? 
----
<!-- 

Network ID. First IP address in each Sub-Network. -     Designates where IP address will start, can not be used by a device
Broadcast IP. Last IP address in each Sub-Network. - Sends data to all devices, can not be used by a device
First Host IP. IP address after the Network ID. - Commonly the router, as its the first device
Last Host IP. IP address before the Broadcast IP. - The last possible IP that can be provided
Next Network. IP address after the Broadcast IP. - The next networks starting IP
# IP Addresses. Number of IP addresses in Sub-Network
CIDR/ Subnet. Converting between CIDR/ Subnet Mask

 -->

* Network ID - First IP address in each Sub-Network - Designates where IP address' will start (not used by any devices)
* Broadcast IP - Last IP address in each Sub-Network - Sends data to all devices (not used by any devices)
* First host IP - IP address after the network ID - Commonly used for the router, as it is the first device (these are used by devices)
* Last host IP - IP address before the Broadcast IP - The last possible IP address that can be provided  (these are used by devices)
* Next Network - IP address after the Broadcast IP - Next Sub-networks starting IP (Their network ID)
* Number of IP Address - Group Size
* CIDR/ to Subnet - Converts CIDR/ (`/24`) to a Subnet Mask (`255.255.255.0`)

----

2. How to use and create a subnet cheatsheet
<!-- 
a. Start with 1, double until 128 (right to left)

b. Subtract top row from 256

c. From /32 (right to left)
 -->


a. Start with 1, double until we reach 128, from right to left

b. Subtract the top from 256

c. From /32, decrease by 1, from right to left

| 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 | - Group Size |
| - | - | - | - | - | - | - | - | - |
| 128 | 192 | 224 | 240 | 248 | 252 | 254 | 255 | - Subnet Mask |
| /25 | /26 | /27 | /28 | /29 | /30 | /31 | /32 | - CIDR |
----

3. Provide two examples in which you demonstrate the use of a subnet cheatsheet.
<!-- 
 1. # IP Addresses - Cheat Sheet
 2. CIDR/ Subnet - 255.255.255.<cheat sheet>
 3. Next Network - Add group size until greater than the last value in the IP
 4. Network ID - Subtract group size from Broadcast ID
 5. Broadcast IP - One less than the Next Network
 6. First Host - Add one to Network ID
 7. Last Host - Subtract one from Broadcast IP
 -->
10.1.1.55/28

1. \# of IP Address (Group Size) - Cheat Sheet
2. CIDR/ to Subnet (`255.255.255.x`) - Cheat Sheet
3. Next Network - Add group size, until it is greater than the last value in the ip
4. Network ID - Subtract the Group Size, from the Next Network
5. Broadcast IP - One Less than the Next Network
6. First Host - Add one the network ID
7. Last host - Subtract one from the broadcast IP

* Network ID: `10.1.1.48`
* Broadcast IP: `10.1.1.63`
* First Host IP: `10.1.1.49`
* Last Host IP: `10.1.1.62`
* Next Network: `10.1.1.64`
* \# IP Addresses: `16`
* CIDR/ Subnet: `255.255.255.240`

<!-- * Network ID.
* Broadcast IP.
* First Host IP.
* Last Host IP.
* Next Network.
* \# IP Addresses
* CIDR/ Subnet. -->

----
10.1.1.37/29

* Network ID: `10.1.1.32`
* Broadcast IP: `10.1.1.39`
* First Host IP: `10.1.1.33`
* Last Host IP: `10.1.1.38`
* Next Network: `10.1.1.40`
* \# IP Addresses: `8`
* CIDR/ Subnet: `255.255.255.248`