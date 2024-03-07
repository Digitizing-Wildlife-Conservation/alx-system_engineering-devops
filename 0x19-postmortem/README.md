0x19. Postmortem DevOps SysAdmin Cohort 

Following a complete outage of our e-commerce website on May 10th, 2023, lasting from 2:30 PM to 5:00 PM (WAT), impacting all services including product listings, shopping cart,
and checkout processes, we identified a memory leak in the web application server as the root cause. Despite initial attempts to restart the server, the issue persisted until the
team discovered the memory leak at 3:00 PM. Subsequent investigation led to the identification of the leak in the code, which was promptly fixed by optimizing the code and improving
memory management practices. The website was restored to full functionality by 4:45 PM. It's worth noting that initial investigations focused on server configuration, delaying the 
identification of the actual problem. The incident was escalated from the operations to the development team once the nature of the issue became clear. To prevent similar occurrences,
we have implemented measures to enhance code efficiency and monitoring protocols.
