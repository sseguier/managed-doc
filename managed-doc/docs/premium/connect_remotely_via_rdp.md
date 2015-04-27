Here are steps to allow remote access to your VM(s)

## Configure vShield router: NAT

 * Go to "administration" tab
 * Select your Virtual Datacenter
 * Go to "Edge Gateways" tab
 * Right click on the vShield router
 * Click Edge gateway services
 * Go to "NAT" tab
 * At the bottom select "DNAT"
 
Applied on: exoGV*_public_network

Original (External) IP/Range: Your public IP

Protocol: TCP 

Original port: 3389

Translated (Internal) IP/Range: Your internal VM ip

Translated port: 3389


Tick: Enabled



In case you want to allow multiple remote access to multiple VM, you should change each time the "Original port".


## Configure vShield router: Firewall

 * Go to "administration" tab
 * Select your Virtual Datacenter
 * Go to "Edge Gateways" tab
 * Right click on the vShield router
 * Click Edge gateway services
 * Go to "Firewall" tab
 * At the bottom select "Add"
 
 
 Tick: Enabled
 
 Name: RDP access (for instance)
 
 Source: 0.0.0.0/24 or more restrictive subnet --> your office
 
 Source port: Any or 3389
 
 Destination: Your public IP
 
 Destination port: Any or 3389
 
 Protocol: TCP
 
 Action: Allow
 
 
 Once you have allowed traffic on port 3389, simply point your remote desktop client to the public IP address of your VM using the username "administrator".
 
 Example: 80.245.22.x:3389
 
