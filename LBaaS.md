### Intro to LBaaS V2

Load Balancing-as-a-Service (LBaaS) enables OpenStack Networking to distribute incoming requests evenly between designated instances. This ensures the workload is shared predictably among instances, and allows more effective use of system resources. Incoming requests are distributed using one of these load balancing methods: 
..* Round robin - Rotates requests evenly between multiple instances. 
..* Source IP - Requests from a unique source IP address are consistently directed to the same instance. 
..* Least connections - Allocates requests to the instance with the least number of active connections. 
    
To get started, navigate to Network -> Load Balancers.

### Building an LBaaS v2 load balancer
Start by creating a load balancer on a network. Provide a load balancer name and select the private subnet that two web server instances reside on.

[[tutorial_screenshots/newton/lb_details.png|LBaaS details]]

### Adding an HTTP listener
Add a listener for plaintext HTTP traffic on port 80. You can also select TCP with specified port number.

[[tutorial_screenshots/newton/lb_listener_details.png|LBaaS listener details]]

### Adding pool details
Add pool details and select one of the load balancing methods
[[tutorial_screenshots/newton/lb_pool_details.png|LBaaS pool details]]

### Adding pool members
Add members to the pool to serve HTTP content on port 80. For this example, the web servers are 192.168.129.7 and 192.168.129.12
[[tutorial_screenshots/newton/lb_pool_members.png|LBaaS member details]]

### Adding a health monitor
Add a health monitor so that unresponsive servers are removed from the pool automatically

[[tutorial_screenshots/newton/lb_monitor_details.png|LBaaS monitor details]]


### Associating a floating IP address

Load balancers deployed onto private network need a floating IP address assigned if they must be accessible to external clients. 

Associating a floating IP to the load balancer
[[tutorial_screenshots/newton/lb_floatingIP.png|LBaaS FloatingIP]]

***
#### Next: [[API Access]]  
###### Previous:  [[SSH to Cloud VM]]
[[Openstack Tutorial Index]]  
