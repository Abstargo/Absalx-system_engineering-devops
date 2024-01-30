# 0. SIMPLE WEB STACK
![a screenshot of web infra](https://github.com/Abstargo/alx-system_engineering-devops/blob/main/0x09-web_infrastructure_design/0-simple_web_stack.PNG)

## Specifics About This Infrastructure

1. ### What is a Server?
   - A single server that hosts the entire web infrastructure.
   - It contains the necessary software components: Nginx web server, application server, and MySQL database.

2. ### Domain Name:
   - The domain name is foorbar.com
   - It contains the necessary software components: Nginx web server, application server, and access the website via www.foorbar.com

3. ### DNS Record for www:
   - The www in www.foobar.com is a subdomain, and it typically corresponds to a CNAME (Canonical Name) DNS record.
   - The CNAME record for www.foobar.com points to the main domain foobar.com, which, in turn, resolves to the server's IP address (8.8.8.8).

4. ### Web Server (Nginx):
   - Nginx serves as the web server in this infrastructure.
   - It handles incoming HTTP requests from users, manages static content, and can act as a reverse proxy to the application server.

5. ### Application Server:
   - The application server (e.g., running a server-side scripting language like PHP, Python, or Node.js) processes dynamic content and business logic.
   - Nginx forwards dynamic requests to the application server for processing.

6. ### Application Files (Code Base):
   - The application files, comprising the code base, are hosted on the server.
   - These files contain the logic and functionality of the website.

7. ### Database (MySQL):
   - MySQL is used as the database to store and retrieve data for the website.
   - The application server communicates with the database to fetch or update information.

8. ### Communication:
   - The server communicates with the user's computer over the HTTP or HTTPS protocols.
   - When a user requests www.foobar.com, the DNS resolution directs them to the server's IP address, and Nginx handles the incoming HTTP request.
   - If dynamic content is needed, Nginx forwards the request to the application server, which interacts with the MySQL database.

## Issues With The Infrastructure:

1. ### Single Point Failure (SPOF):
   - The entire infrastructure relies on a single server (8.8.8.8), which is a potential single point of failure. If the server goes down, the entire website becomes inaccessible.

2. ### Downtime during Maintenance:
   - Deploying new code or performing maintenance tasks may require restarting the web server. During this time, the website may experience downtime.

3. ### Scaling Limitations:
   - The current infrastructure may struggle to handle a sudden increase in incoming traffic. Scaling options, such as load balancing and distributing the workload across multiple servers, are not implemented in this design.