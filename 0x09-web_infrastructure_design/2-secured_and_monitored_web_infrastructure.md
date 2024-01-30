# 2. Secured and monitored web infrastructure

![](https://github.com/Abstargo/alx-system_engineering-devops/blob/main/0x09-web_infrastructure_design/2-secured_and_monitored_web_infrastructure.PNG)

# Description

This a 3-Server web infrastructure that is secured, monitored, and servers encrypted traffic.

## Specifics About This Infrastructure

### 1. The purpose of the firewalls:
    The firewalls are for protecting the network (web servers, anyway) from unwanted and unauthorized users by acting as an intermdiary between the internal network and the external network and blocking the incoming traffic matching the aforementioned criteria.
### 2. The purpose of the SSL certificate:
    The SSL certificate is for encrypting the traffic between the web servers and the external network to prevent man-in-the-middle attacks (MITM) and network sniffers from sniffing the traffic which could expose valuable information. The SSL ensure privacy, integrity, and identification.
### 3. The purpose of the monitoring clients:
    The monitoring clients are for monitoring the servers and the external network. They analyse the preformance and operations of the servers, measure the overall health, and alert the administrators if the servers are not performing as expected. The monitoring tool observes the servers and provides key metrics about the servers' operations to the administrators. It automatically tests the accessibility of the servers, measures response time, and alerts for errors such as corrupt/missing files, security vulnerabilities/violations, and many other issues.

## Issues with the Infrastructure:

### 1. Terminating SSL at Load Balancer:
    Terminating SSL at the load balancer means that the communication between the load balancer and the web servers is unencrypted. It might expose sensitive data if it's transmitted over internal networks. It's generally recommended to use end-to-end encryption for improved security.
### 2. Single MySQL Server Accepting Writes:
    Having only one MySQL server capable of accepting writes introduces a single point of failure. If this server fails, write operations would be disrupted, affecting the availability of the system.
### 3. Uniform Servers With All The Same Components:
    Having servers with identical components may lead to a lack of diversity, making the entire infrastructure vulnerable to common vulnerabilities or threats. Diversifying components and configurations can enhance resilience against certain types of attacks or failures.