## About This Infrastructure

+ What is a server??<br/>
In the context of web infrastructure, a server refers to a machine or software that hosts and serves web content, applications, and services over the Internet.<br/>
Servers play a critical role in the functioning of modern computer networks and the internet. They enable the delivery of various services and resources to clients, allowing for efficient communication and collaboration across different devices and locations.

+ The role of the domain name.<br/>
The domain name plays a crucial role in identifying and locating resources on the internet. It serves as a human-readable and memorable address for websites, email servers, and other online services.
For example, the domain name `www.google.com` is easier to recognize and remember than an IP address`142.250.217.78`. The IP address and domain name alias are mapped in DNS (the Domain Name System)

+ The type of DNS record `www` is in `www.foobar.com`.<br/>
An A record is used to map a hostname (in this case, "www") to the corresponding IPv4 address of the server that hosts the website. When a user enters "www.foobar.com" in their web browser, the DNS system looks up the A record for the "www" subdomain and retrieves the associated IPv4 address. This allows the browser to establish a connection with the correct server and retrieve the requested web pages.

+ The role of the web server.<br/>
the web server acts as the intermediary between clients and the web application or content they are requesting, can be via HTTP or secur HTTP(HTTPS).  It manages the delivery of web content, handles requests, processes dynamic content, and ensures secure and efficient communication between clients and the server.

+ The role of application server.<br/> The application server it is responsible for running and executing the application code that powers dynamic web applications.

+ The role of the database.<br/> it is responsible for storing, organizing, and managing structured data used by web applications

+ What the server uses to communicate with the user (computer of the user requesting the website).<br/>the server uses the HTTP protocol to facilitate communication with the user's computer. It handles the requests, processes them, generates appropriate responses, and transmits the responses back to the user, allowing the web browser to render and display the requested content.

## Issues With This Infrastructure

+SPOF(single point of failure) <br/>  A Single Point of Failure refers to a component or system that, if it fails, can cause the entire infrastructure or service to become unavailable.

In this case, the infrastructure consists of a single server hosting the website, which means that if the server fails or experiences any issues, the website will be inaccessible. This creates a SPOF because there is no redundancy or backup system in place to ensure continuous availability in case of server failure.

+Downtime when maintenance needed<br/>Another issue with this infrastructure is downtime when maintenance is needed. Whenever maintenance activities, such as deploying new code or performing updates, are required on the web server, it often requires taking the server offline or restarting it. This downtime can result in the website being temporarily unavailable to users.

+ cant scale if too much incoming traffic<br/> Other issue with this infrastructure is the inability to scale effectively when there is a significant increase in incoming traffic. the single server may struggle to handle the increased load, leading to performance issues and potentially causing the website to become slow or even unresponsive.
