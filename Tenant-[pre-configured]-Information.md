# Accounts
There will be two accounts:
* \<tenant\>_admin :  tenatn admin, able to create, update, delete the resource
* \<tenant\>_user :   tenant user, able to access the resource but cannot modify them

# Network
There are two floating IP range: 
* \<tenant\>_public: 175.159.190.0/24 which is internet accessible, there will be external firewall
  + \<tenant\>_private: 192.168.65.0/24, connected to \<tenant\>_public by router \<tenant\>_router
* \<tenant\>_public_vlan184:10.99.x.0/24 which is not internet accessible, and there will be no external firewall blocking.
  + \<tenant\>_private_vlan184: 192.168.129.0/24, connected to \<tenant\>_public_vlan184 by router \<tenant\>_router_vlan184


