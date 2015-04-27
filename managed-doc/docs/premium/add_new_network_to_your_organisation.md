In order to add a new network to you tenant or organization, follow this guide:

## Zone choice 

### Each customer can choose the number of zones available in is tenant

 * 1 zone
 * 2 zones*

### Mutiple zones can be connected:
 
 * Via selfservice IpSec VPN directly from exorun premium interface

![VPN connection](/static/images/kb/add_network-1.png)

 * Via dedicated and reserved capacity link between zones. Contact sales@exoscale.ch to order.

### Purpose: With 2 zones one can build a H/A or DRP compliant architecture


 * NOTE: 2 zones implies 1 additional public IP billed.


## Multiples zones setup on Exoscale

A zone is a separate datacenter implementation of Exoscale premium

Zone are most often in different locations and are prefixed with the datacenter initials:

 * Ex: GV = Geneva

## 3 network options are available on Exoscale premium

 * Default subnet creation
 * Custom subnet range
 * Complex network setting

Each option can receive additional public IPs. You can specify them in your request or add them later by contacting [SUPPORT](mailto:support@exoscale.ch)

### Default subnet:

If you select the default network setting you will get per zone:
 * 1 public IP
 * 1 Firewall with all inbound* ports closed. Outbound ports opened.
 * 1 subnet range with the following settings:
    * Network address: 10.0.x.0 with x the ID of the zone
    * Netmask: 255.255.255.0
    * Gateway: 10.0.x.1

Instances network assignment can be:

 * DHCP
 * Static but allocated by Exoscale premium
 * Static and manually set up

NOTE: NAT or PAT features requires at least 1 additional public IP.

![VPN connection](/static/images/kb/add_network-2.png)

### Custom subnet range:

If you select a custom network setting you will get per zone:

 * 1 public IP
 * 1 Firewall with all inbound* ports closed. Outbound ports opened.
 * 1 subnet range for which you must specify:
    * Network address: private IPv4
    * Netmask
    * Gateway
    * DHCP feature: yes/no
    * If yes specify first and last IP

![VPN connection](/static/images/kb/add_network-3.png)

### Complex network setting:

The following setups are possible. Please provide a basic schematic with all ranges along with your request.

![VPN connection](/static/images/kb/add_network-4.png)
