# Systems Design

## System Properties:
### You want your System to be:

+ Secure: authentication, authorization, accounting (aaa)
+ Reliable: slow to fail

+ Robust:  quick to recover from failure.

+ Highly Available: 99.999%
+ Performant: speed/latency
+ Scalable: capacity/bandwidth
+ Maintainable: automation
+ Cost Effective:  minimize Capex & Opex

Every business has business goals.

These ***System Properties*** align with the typical high level business goal of ***"satisfy your customers"***.

### Your System is a Stack comprised of Layers:

* Data Layer:
* Network Layer:
* Compute Layer:
* Personnel Layer: all the departments and teams that are your business.

In order to achieve the above ***System Properties*** you have to apply the ***"best practices"***, and the ***"best technologies"*** for each property, at each layer of your stack.

This is a daunting task because there are so many options available and so many different ways your system will behave depending on the choices you make for each property at each layer.

The permutations of choices and behavior quickly explode combinatorally.

This is what makes your System ***"complex"***; and why it typically requires a qualified ***System Designer*** to achieve your goals.

### So where do you begin?

It always starts with understanding your workload.

You can't make the ***"best choices"*** without understanding your workload intimately and ***testing*** thoroughly.

Starting from a blank slate is different than inheriting an existing system infrastructure.

### Here are some System Design questions to get you started:

### System Design Questions:

+ How do you make decisions regarding all of the questions below?
  - Who are your Architects/Designers?
  - How do you find the ***right balance*** between all the ***trade-offs*** during the design process?
  - How do you choose the right Data Design?
  - How do you choose the right Database?
  - How do you choose the right Network Design?
  - How do you choose the right Compute Design?
  - How do you choose the best Cloud Provider?
+ How do your Teams/Departments communicate:
  - Email, Chat, Video: Office365, Slack, MSTeams, Zoom, WebEx, GoToMeeting?
+ What Security Policies do you have?
  - What Security Tools do you use?
+ How do you Monitor your System?
  - What Monitoring Tools do you use?
    - Grafana, Prometheus, Cloudwatch, CloudTrail
+ How do you Process your Logs?
  - What Logging Tools do you use?
    - Splunk, Datadog, Graylog, etc.
+ OnPrem, Cloud, MultiCloud or Hybrid?
  - What Cloud Platform(s) and Services do you use?
    - AWS has over 535 Cloud Services spanning TBD Categories https://www.antvaset.com/c/21gjdl7gz4
    - GCP has over 32 Cloud Services spanning 7 Categories https://cloud.google.com/products/ https://www.infiflex.com/what-are-the-google-cloud-platform-services
    - Azure has over 295 Cloud Services spanning 21 Categories https://azure.microsoft.com/en-us/products/
  - Where are your High-Level Architecture/Design Diagrams?
+ Cloud Agnostic or Cloud Native?
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
+ What Infrastructure Tools do you use?
  - Terraform, Ansible, Nomad, Kubernetes?
+ What, When, How and Why do you Test?
  - What Testing Tools do you use?
+ What is your Network Design?
  - Where are your Network Architecture Diagrams?
  - Describes your Network: Traffic Ingress/Egress, Routers, Switches, Firewalls, Load Balancers, API Gateways, iPXE, NTP/PPT, DNS, DHCP, BGP (eBGP,iBGP), OSPF; CDNs, Edge Networking; Failover, Redundancy, etc.
+ What Network Tools do you use?
  - RANCID, Kubespray, Kubernetes Dashboard, etc.
+ What is your Data Design?
  - Data Lake, Wherehouse, Data Catalog
  - Relational, NoSQL, Document Oriented, Graph DB
  - Block Storage, Filesystem Storage, Object Storeage
  - CePH, BitTable, DynamoDB, etc.
  - Snapshots, Replication, Backups, Data Migration
+ What Data Tools do you use?
+ ***and many many more things to consider. I told you it was complicated***
