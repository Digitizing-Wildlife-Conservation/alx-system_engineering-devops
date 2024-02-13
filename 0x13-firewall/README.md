0x13. Firewall DevOps SysAdmin Security Cohort

In the Firewall DevOps SysAdmin Security Cohort project, I Moses Muchai, a DevOps Engineer, utilized the ufw tool to establish firewall configurations on the assigned web servers.
 
The primary objectives included blocking all incoming traffic with specific exceptions and implementing port forwarding.

For the task "Block all incoming traffic but," Moses developed a Bash script titled 0-block_all_incoming_traffic_but to enact a ufw firewall setup.
This script ensures that incoming traffic is restricted, permitting access solely through ports 22, 443, and 80 on the web server.

In the subsequent task "Port forwarding," I Moses created a ufw configuration file named 100-port_forwarding to facilitate the redirection of traffic
from port 8080/TCP to port 80/TCP effectively. This configuration enhances the network setup to efficiently manage incoming connections while maintaining security measures.
