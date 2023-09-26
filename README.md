# Systems Design

## System Properties:
### You want your System to be:

+ Secure: authentication, authorization, accounting (aaa); Zero-Trust
+ Reliable: slow to fail
+ Robust:  quick to recover from failure.
+ Highly Available: 99.999% uptime
+ Performant: speed/latency
+ Scalable: capacity/bandwidth
+ Maintainable: automation
+ Cost Effective:  minimize Capex & Opex

Every business has business goals.

These ***System Properties*** align with the typical high level business goal of ***"satisfy your customers"***.

### Your System is a Stack comprised of Layers:

* Storage/Data Layer:
* Network Layer:
* Compute Layer:
* Personnel Layer: all the departments and teams that are your business.

In order to achieve the above ***System Properties*** you have to apply the ***"best people"***, applying the ***"best practices"***, using the ***"best technologies"*** for each property, at each layer of your stack.

This is a daunting task because there are so many options available and so many different ways your system will behave depending on the choices you make for each property at each layer.

The permutations of choices and behavior quickly explode combinatorally.

This is what makes any System ***"complex"***; and why it typically requires a qualified ***System Designer*** to achieve your goals.

### So where do you begin?

It always starts with understanding your workload.

You can't make the ***"best choices"*** without understanding your workload intimately and ***testing*** it thoroughly.

Starting from a blank slate is different than inheriting an existing system infrastructure.

### Here are some System Design questions to get you started:

### System Design Questions:
+ Definitions:
  - Infrastructure: The physical resources that support your environment, includes: Data Centers, Platforms, Systems, Workloads, People.
  - Data Center: A Physical Building located around the world that houses your Platfoms, Systems, Workloads.
  - Platform: The logical term that support your environment: OnPrem, Cloud, MultiCloud or Hybrid?
  - System: the collection of components (hardware,software,people) that interact together to implement your Platform.
  - Workload: the main application your customers interact with (aka., your "Product").
  - People: all your employess across all of your departments: IT/SRE/DevOps/Platform Engineers/Secuirty Specialists/Programmers; Sales, Marketing
+ How do you make decisions regarding all of the questions below?
  - Who are your Architects/Designers?
  - How do they strike the ***right balance*** between all the ***trade-offs*** during the design process?
  - How do they choose the best Platform Design, Tools and Practices for your Workload?
  - How do they choose the best UX/UI/Frontend Design, Tools and Practices for your Workload?
  - How do they choose the best Storage/Database/Data Design, Tools and Practices for your Workload?
  - How do they choose the best Network Design, Tools and Practices for your Workload?
  - How do they choose the best Compute Design, Tools and Practices for your Workload?
  - How do they choose the best Data Structures, Algorithms and Protocols for your Workload??
  - How do they choose the best Security Design, Tools and Policies/Practices for your Workload?
  - How do they choose the best Observability/Telemetry/Monitoring/Logging/Analytics Design, Tools and Practices for your Workload?
  - How do they choose the best Testing/Benchmarking Design, Tools and Practices for your Workload?
  - How do they choose the best Programming Language, IDE, etc. to implement your Workload?
  - How do they choose the best SDLC, CI/CD, and Distributed Version Control System Design, Tools and Practices for your Workload?
+ How do your Architects/Designers/Programmers/Teams/Departments communicate:
  - Email, Chat, Slack, Video: Office365, MSTeams, Zoom, WebEx, GoToMeeting?
+ What Environment/Platform does your workload run?
  - OnPrem, Cloud, MultiCloud or Hybrid?
  - Cloud Agnostic/Cloud Native?
  - Self-Hosted/Fully Managed?
  - What Cloud Platform(s) and Services do you use?
    - AWS has over 535 Cloud Services spanning TBD Categories https://www.antvaset.com/c/21gjdl7gz4
    - GCP has over 32 Cloud Services spanning 7 Categories https://cloud.google.com/products/ https://www.infiflex.com/what-are-the-google-cloud-platform-services
    - Azure has over 295 Cloud Services spanning 21 Categories https://azure.microsoft.com/en-us/products/
  - Where are your High-Level Architecture/Design Diagrams?
+ What Security Policies do you implement?
  - What Security Tools do you use to implement those Security Policies?
+ What Observability Best practices do you use?
  - What Observability Tools do you use?
+ What Telemetry/Metrics to you gather?
  - What Analytics Tools do you use?
+ How do you Monitor your System/Workload?
  - What Monitoring Tools do you use?
+ How do you Process your Logs?
  - What Logging Tools do you use?
+ Open Source Software or Enterprise Software?
+ Bare Metal, VMs, Containers?
+ Monolithic, Microservices, Serverless?
+ Request-Response (Synchronous) or Event-driven (Asynchronous)?
+ Multitenant or Single Tenant?
+ What Programming Languages do you use?
  - Python, Go, C, C++, Java, etc.
+ What Programming Tools do you use?
  - IDEs, Git, Programming Style Guides, etc.
+ What is your SDLC, CI/CD, Deployment strategy (Rolling, Canary, Blue-Green)
+ What Infrastructure Provisioning Tools do you use?
  - Terraform, Ansible, Nomad, Kubernetes?
+ What, When, How and Why do you Test?
  - What Testing Tools do you use?
+ What is your Network Design?
  - Where are your Network Architecture Diagrams?
  - Describes your Network: Traffic Ingress/Egress, Routers, Switches, Firewalls, Load Balancers, API Gateways, iPXE, NTP/PPT, DNS, DHCP, BGP (eBGP,iBGP), OSPF; CDNs, Edge Networking; Failover, Redundancy, etc.
+ What Network Tools do you use?
  - RANCID, Netcat, Netbox, iperf, etc.
+ What is your Storage/Data Design?
  - Where are your High-level Storage/Data Architecture/Design Diagrams?
  - Data Lake, Wherehouse, Data Catalog
  - Relational, NoSQL, Document Oriented, Graph DB
  - Block Storage, Filesystem Storage, Object Storeage
  - CePH, BigTable, DynamoDB, etc.
  - Snapshots, Replication, Backups, Data Migration
+ What Data Tools do you use?
+ What is your Compute Design?
  - Where are your High-level Compute Design Diagrams?
  - AWS EC2 VMs, OnPrem Servers/VMs, etc.
+ ***and many many more things to consider. I told you it was complicated***
