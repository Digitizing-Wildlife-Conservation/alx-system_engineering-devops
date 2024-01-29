0x0F. Load balancer DevOps SysAdmin Cohort 


Load Balancer

Overview

In this project, we focus on enhancing our web stack by introducing redundancy for our web servers. By doubling the number of web servers and implementing a load balancer, we aim to handle more traffic and ensure infrastructure reliability. The project, involves configuring two additional servers: gc-[STUDENT_ID]-web-02-XXXXXXXXXX and gc-[STUDENT_ID]-lb-01-XXXXXXXXXX. Bash scripts are utilized to automate the configuration of brand new Ubuntu servers according to the specified requirements.

Task 0: Double the Number of Webservers
The initial task involves configuring web-02 to be identical to web-01. A Bash script, 0-custom_http_response_header, is created to configure Nginx on both web servers to include a custom HTTP response header (X-Served-By), indicating the hostname of the server Nginx is running on. This customization aids in tracking the web server responsible for handling HTTP requests, providing insights into load balancer functionality.

Task 1: Install Your Load Balancer
The second task focuses on installing and configuring HAproxy on the lb-01 server. The Bash script, 1-install_load_balancer, ensures that HAproxy is configured with a version equal to or greater than 1.5, sending traffic to web-01 and web-02 using a round-robin algorithm. The script also enables HAproxy management via an init script, ensuring servers are configured with the correct hostnames.

Task 2: Add a Custom HTTP Header with Puppet (Advanced)
Building on the concept of automating custom HTTP header configuration, Task 2 involves using Puppet. The Puppet script, 2-puppet_custom_http_response_header.pp, is designed to configure a new Ubuntu machine to meet the specified requirements for the custom HTTP header (X-Served-By).

Repository Information
GitHub Repository: alx-system_engineering-devops
Directory: 0x0F-load_balancer
Files:
0-custom_http_response_header
1-install_load_balancer
2-puppet_custom_http_response_header.pp
Explore the repository for detailed implementation and scripts related to load balancing and web stack improvements.
