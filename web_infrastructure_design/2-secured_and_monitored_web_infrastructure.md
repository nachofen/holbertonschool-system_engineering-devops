# Specifics About This Infrastructure

## The purpose of the firewalls.
The purpose of firewalls is to protect a computer network by establishing a security barrier between the internal network and external networks, such as the Internet. They act as a traffic filter, allowing or blocking certain communications based on predefined rules.
## Why is the traffic served over HTTPS
Traffic is served over HTTPS (Hypertext Transfer Protocol Secure) to ensure the secure transmission of data between a web server and a client's browser.
## What monitoring is used for
monitoring is essential for maintaining the health, performance, and security of web infrastructure. It enables proactive management, timely issue resolution, and continuous improvement of IT operations.
# Explain what to do if you want to monitor your web server QPS
first we should choose wich montoring tool we are going to use, it must support web server monitoring and provide QPs metrics. then we would have to install it on the web server. we also should define wich QPS metric are going to use and finally set interval, thresholds and alerts
# Issues With This Infrastructure

## Terminating SSL at the load balancer level
first, we have the security: Decrypted traffic between the load balancer and backend servers is vulnerable to interception or manipulation.<br/>
then cmpliance: It may violate compliance requirements that mandate end-to-end encryption for data in transit.<br/>
Client IP Preservation: Backend servers see client requests as coming from the load balancer's IP, affecting functionality relying on client IP, such as geolocation or access controls
and finally Load balancer downtime or failure impacts all traffic to backend servers.
## Why having only one MySQL server capable of accepting writes is an issue?
Having only one MySQL server capable of accepting writes can be problematic due to a single point of failure, limited scalability, lack of redundancy, challenges in maintenance and upgrades, difficulties in disaster recovery, and potential performance bottlenecks. Implementing strategies like replication, clustering, or sharding can address these issues and provide improved availability, scalability, and data protection.
## Why having servers with all the same components (database, web server and application server) might be a problem?
Having servers with all the same components (database, web server, and application server) can lead to issues such as inefficient resource utilization, difficulties in scaling specific components, increased maintenance complexity, higher costs, and limited technology flexibility. It is important to consider the unique requirements of each component and design server configurations accordingly for optimal performance and resource allocation.
