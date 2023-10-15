# ansible__

In this assignment, a simple application in python-flask known as application.py is implemented and put it behind the HAproxy- which acts as a load balancer between the 3-dev servers namely devA, devB, and devC. A Bastion host is created which acts as an SSH entry point into the whole network.
There are total of 5 servers deployed using city cloud. Floating IPs are provided to the host BastionNSO and HAproxy while Dev servers have only private IP addresses. We use ansible-playbook "site.yaml" to deploy the flask application on dev servers and to do load-balancing among them we deploy the haproxy load balancing configuration file.
UDP-Load Balancing using Nginx is achieved. In this case, HAproxy takes care of the flask app while nginx takes care of snmp in all the servers.
For testing we simply curl to haproxy's ip address and it should reply with the time and hostname of the host that replied. 
