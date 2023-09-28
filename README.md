# Systems Design

## System Properties:
### You want your System to be:

+ Secure: authentication, authorization, accounting (aaa); Zero-Trust
+ Reliable: slow to fail
+ Robust:  quick to recover from failure.
+ Highly Available: 99.999% uptime
+ High Performance: maximize speed/latency
+ Scalable: maximize capacity/bandwidth (take advantage of Economy of Scale)
+ Maintainable: maximize "frictionless automation"
+ Cost Effective:  minimize Capex & Opex

Every business has business goals.

These ***System Properties*** align with the high level business goal of ***"satisfy your customers"***.

### Your System is a Stack comprised of Layers:

* Storage/Data Layer:
* Network Layer:
* Compute Layer:
* Personnel Layer: all the departments and teams that are your business.

In order to achieve the above ***System Properties*** you have to apply the ***"best people"***, applying the ***"best practices"***, using the ***"best technologies"*** for each property, and at each layer of your stack (I call this ***"Full Stack"*** implementation).

This is a daunting task because there are so many choices available and so many different ways your system will behave depending on the choices you make for each property at each layer.

The permutations of choices and behavior quickly explode combinatorally.

This is just one of the causes that makes any System ***"complex"***; and why it requires a qualified ***System Designer*** to achieve these ***System Properties***.
Other causes of complexity include: non-linear dynamics, chaotic behavior, randomness (difficult to predict), a deep nesting of many layers of abstraction, etc. which are all symptoms of the combinatorial explosion I already mentioned.

### So where do you begin?

It always starts with understanding your workload.

You can't make the ***"best choices"*** without understanding your workload intimately and ***testing*** it thoroughly.

Starting from a blank slate is different than inheriting an existing system infrastructure.

### Here are some System Design questions to get you started:

### System Design Questions:
+ Definitions:
  - Infrastructure: The physical resources that support your environment, includes: Data Centers, Platforms, Systems, Workloads, People.
  - Data Center: A Physical Building located around the world that houses your Platforms, Systems, Workloads.
  - Platform: The logical term that supports your environment: OnPrem, Cloud, MultiCloud or Hybrid?
  - System: the collection of components (hardware,software,people) that interact together to implement your Platform.
  - Workload: the main application your customers interact with (aka., your "Product and/or Service").
  - People: all your employess across all of your departments: Platform Engineers/SREs/DevOps/DevSecOps/Programmers; Sales, Marketing
+ How do you make decisions regarding all of the questions below?
  - Who are your Architects/Designers?
  - Where are their High-Level Architecture/Design Diagrams?
  - How do they strike the ***right balance*** between all the ***trade-offs*** during the design process?
  - How do they define clear objectives?
  - How do they measure success?
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
  - How do they choose the best SDLC, CI/CD, and Distributed Version Control System Design, Tools and Practices/Workflows for your Workload?
+ How do your Architects/Designers/Programmers/Teams/Departments communicate and how often?
  - In person Meetings, Email, Mailing Lists, Chat, Slack, Mastadon, IRC; Video: Office365, MSTeams, Zoom, WebEx, GoToMeeting?
  - Every week, Daily (15 min scrum), every month, never?
+ What Environment/Platform does your workload run?
  - OnPrem, Cloud, MultiCloud or Hybrid?
  - Bare Metal, VMs, Containers, Mixture of All of them?
  - Cloud Agnostic/Cloud Native?
  - Self-Hosted/Fully Managed?
  - Open Source Software/Enterprise Software?
  - Monolithic, Microservices, Serverless?
  - Request-Response (Synchronous)/Event-driven (Asynchronous)?
  - Multitenant/Single Tenant?
  - What Cloud Platform(s) and Services do you use?
    - AWS has over 535 Cloud Services spanning 20+ Categories https://www.antvaset.com/c/21gjdl7gz4
    - GCP has over 32 Cloud Services spanning 7 Categories https://cloud.google.com/products/ https://www.infiflex.com/what-are-the-google-cloud-platform-services
    - Azure has over 295 Cloud Services spanning 21 Categories https://azure.microsoft.com/en-us/products/
+ What is your Disaster Recovery Plan (DRP)?
  - How often to you practice your DRP?
  - How do you Failover your workload?
  - What are your Incidence Response and Root Cause Analysis (RCA) procedures.
+ What is your Network Design?
  - Where are your High-Level Network Architecture/Design Diagrams?
  - Describes your Network: Traffic Ingress/Egress, Routers, Switches, Firewalls, Load Balancers, API Gateways, iPXE, NTP/PPT, DNS, DHCP, BGP (eBGP,iBGP), OSPF; CDNs, Edge Networking; Failover, Redundancy, etc.
  - What Network Tools do you use?
    - RANCID, Netcat, Netbox, iperf, etc.
+ What is your Storage/Data Design?
  - Where are your High-level Storage/Data Architecture/Design Diagrams?
  - Data Lake, Wherehouse, Data Catalog
  - Relational, NoSQL, Document Oriented, Graph DB
  - Block Storage, Filesystem Storage, Object Storage
  - CePH, BigTable, DynamoDB, etc.
  - How do you snapshot/replicate/migrate/backup large amounts of data?
  - What Data Tools do you use?
    - DataDog, Splunk, Greylog, etc.
+ What is your Compute Design?
  - Where are your High-level Compute Architecture/Design Diagrams?
  - AWS EC2 VMs, OnPrem Servers/VMs, etc.
+ What Infrastructure Provisioning Tools do you use?
  - Terraform, Ansible, Nomad, Kubernetes?
+ What Programming Languages do you use?
  - Python, Go, Bash, C, C++, Java, Javascript, etc.
  - What Programming Tools and/or Frameworks do you use?
    - IDEs: VSC, Vim, EMacs
    - Distributes Version Control System: Git
    -  Programming Style Guides
    -  Frameworks: Angular, Kafka, React, Backbone, etc.
+ What is your SDLC, CI/CD Workflow?
  - What SDLC, CI/CD Tools do you use?
    - CircleCD, ArgoCD, Jenkins
+ What is your Deployment Strategy?
  - Rolling, Canary, Blue-Green
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
+ What, When, How and Why do you Test?
  - What Testing Tools do you use?
+ What is your Continuous Learning/Improvement Strategy?
  - How much time a week do you spend keeping up on the latest technology?
+ ***and many many more things to consider. I told you it was complicated***

## So what are the next steps?
+ Read the System Design Topics information below which adds more details to what we've already discussed above.
+ Read my -->Kubernetes<-- information.

## System Design Topics:

### System Property Definitions:



### Computer Abstractions:


### Principles of GitOps:
  1) Declarative:
     A system managed by GitOps must have it's state expressed declaratively.
  2) Versioned and Immutable:
     Desired state is stored in a way that enforces immutability,
     versioning and retains a complete version history.
  3) Pulled Automatically:
     Software agents automatically pull the desired state declarations from the source.
  4) Continuously Reconciled:
     Software agents continuously observe actual system state
     and attempt to apply the desired state.

### Three Levels of Maturity for Infrastructure Automation:
  1) Ad-hoc:
     A mix of manual, scripted and niche infrastructure methods.
     People-intensive and error-prone.
  2) Automated:
     Enables infrastructure to be created, administrated and supported without needing increasing numbers of experts who are in high demand and short supply.
  3) Frictionless:
     Consistent, simple, measurable and secure infrastructure automation.
     Removes all manual work, reduces complexity and fragmentation, ensuring the infrastructure is governed, secure and accountable to the business.
     
### Steps to Secure Your CI/CD Pipelines 
  1) Security IN the Pipeline: (SIP)
     SIP involves ensuring developers are not shipping anything inherently insecure into production.
     Therefore, whatever code flows through the CI/CD pipeline must be vetted to ensure it has no security flaws or misconfigurations.
  2) Security OF the Pipeline: (SOP)
     SOP has to do with the security of the software delivery chain itself. 
     SOP focuses on the security posture of the actual systems and tools that compromise the software delivery chain.
  3) Security Around the Pipeline: (SAP)
     SAP is necessary to ensure that attackers can't push code directly into production.
     An example, no single developer can publish to production unless approved by two reviewers.

### Advantages of Event-Driven Architectures (EDAs)
  EDAs are a way of designing and building systems that are based on the exchange of events.
  Events are notifications of some change in state or data, and they are typically published by one component and consumed by another in real time.
  EDAs can:
  1) Decouple systems that can be independently scaled and updated.
  2) Handle high volumes of data with low latency.
  3) Support real-time processing and analytics.
  4) Be more scalable and resilient to failures.

### Advantages of Microservices over Monoliths
  1) 
  2) 

### HOWTO: Use AI/ML/DL to Improve the Speed, Accuracy and Clarity of your Platform
  See: AI-ML-DL-in-Platform-Engineering
  1) Use LLMs to Write Boilerplate Code: This accelerates the code writing experience.
  2) Use LLMs to Analyze Logs and other Critical Data: This helps predict future possible outages.
  3) Use LLMs to Analyze Business Data: This helps minimize CapEx and Opex.
  4) Use LLMs to Analyze Customer Data: This helps your customers become more product and leads to a higher level of customer satisfaction.
     

