### Intro to LBaaS V2

Load Balancing-as-a-Service (LBaaS) enables OpenStack Networking to distribute incoming requests evenly between designated instances. This ensures the workload is shared predictably among instances, and allows more effective use of system resources. Incoming requests are distributed using one of these load balancing methods: 
 Round robin - Rotates requests evenly between multiple instances. 
 Source IP - Requests from a unique source IP address are consistently directed to the same instance. 
 Least connections - Allocates requests to the instance with the least number of active connections. 
    
To get started, navigate to Network -> Load Balancers.

### Building an LBaaS v2 load balancer
Start by creating a load balancer on a network. In this example, the private network is an isolated network with two web server instances

[[tutorial_screenshots/newton/lb_details.png|LBaaS details]]

### Adding an HTTP listener
Add a listener for plaintext HTTP traffic on port 80

[[tutorial_screenshots/newton/lb_listener_details.png|LBaaS details]]

### Building a pool and 
You can begin building a pool and adding members to the pool to serve HTTP content on port 80. For this example, the web servers are 192.168.129.7 and 192.168.129.12

[[tutorial_screenshots/newton/lb_pool_details.png|LBaaS details]]

### Adding a health monitor
You can add a health monitor so that unresponsive servers are removed from the pool:
[[tutorial_screenshots/newton/lb_monitor_details.png|LBaaS details]]


### Associating a floating IP address

Load balancers that are deployed on a public or provider network that are accessible to external clients do not need a floating IP address assigned. External clients can directly access the virtual IP address (VIP) of those load balancers.
However, load balancers deployed onto private or isolated networks need a floating IP address assigned if they must be accessible to external clients. To complete this step, you must have a router between the private and public networks and an available floating IP address.
[[tutorial_screenshots/newton/lb_floatingIP.png|LBaaS details]]

***
#### Next: [[API Access]]  
###### Previous:  [[SSH to Cloud VM]]
[[Openstack Tutorial Index]]  
