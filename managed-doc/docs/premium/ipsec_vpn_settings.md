Here are the settings that vCloud Director applies on Exoscale Managed Cloud


## VPN Configuration 

 * Go to "administration" tab
 * Select your Virual Datacenter
 * Go to "Edge Gateways" tab
 * Right click on the vShield router
 * Click Edge gateway services
 * Go to "VPN" tab
 * At the bottom select "add"

## IKE Proposal - phase 1

 * Authentication Method: Mutual PSK (Pre-Shared Key)
 * Encryption: AES256
 * Hash: SHA1
 * Diffie Hellman Group: 2
 * Nat Transversal: Enabled
 * Lifetime: 28800
 * IKE Mode: Main
 * PFS D-H Group: 2
 * Dead Peer Detection: Enabled

## IPSEC Proposal - phase 2

 * Mode: Tunnel
 * Protocol: ESP
 * ESP Encryption: AES-256
 * ESP Authentication: SHA1
 * Lifetime: 3600
 * Perfect Forward Secrecy: Enabled Group 2 (1024bit)

 
N.B.: You have the ability to add multiple peer networks (aka proxy-id), Subnets should be entered in CIDR format with comma as separator in "Peer Networks" field.
 
IPSec VPN tunnels with vShield have been successfully tested with Cisco ASA/IOS, Juniper, Checkpoint, Fortinet appliances and should work with any IPSec compliant hardware or software using the above settings.
