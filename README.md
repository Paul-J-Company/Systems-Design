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

### Your System is a Stack comprised of Abstract Layers:

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

### Design Principles
1) Design is about making tradeoffs and compromises at all levels of your System.
   e.g., Security vs. Convenience, Capex vs. Opex, etc.
2) Define Clear Objectives
3) Define How you Measure Success
4) Efficient Communication:
   ABC = Accurate, Brief and Clear
   CCC = Correct, Concise, Clear
5) Keep it Simple Stupid: (KISS)
   Complexity is the enemy of clarity!
6) Separation of Concerns: (SoP)
7) Single Responsibility Principle: (SRP)
8) Abstraction: See: "Computer Abstractions"

### Computer Abstractions:
I use the terms Layers and Levels interchangably.
In other words, Layers and Levels are synonyms/equivalent.
As mentioned above "Your System is a Stack comprised of Abstract Layers".
Every layer has it's own language/vocabulary/terms/nomenclature.
Every layer produces and Emergent Higher Layer by defining an Interface.
An Interface is the location where objects interact/couple/etc.
I call the combination of all the Layers of your System the "Full Stack".
*) Abstraction:
   TBD
   Information Hiding:
   Encapsulation:
   Modularity:
   Markov Blanket:
   Coupling:
   Cohesion:
1) One-to-Many Abstraction:
   Appears and behaves like one thing, but is actually many things.
     Network:
       Load Balancer:
       API Gateway:
       1-to-Many NAT/PAT:
       Forward Proxy:
       Reverse Proxy:
       HSRP/VRRP/CARP:
       LAG/LACP: aka., NIC Bonding/Teaming/Trunking/Bundling/Channeling
       MLAG:
     Storeage:
       RAID:
       CRUSH:
     Compute:
       Cluster:
2) Local-Remote Abstraction:
   Appears and behaves like a local resource, but is actually a remote resource. 
     Storage:
       NFS:
       SMB/CIFS:
     Compute:
       API:
3) Emulation/Simulation/Virtualization Abstraction:
   Appears and behaves like one thing, but is actually another.
     Network:
       Software:
         OS:
           Virtual Routing and Forwarding: (VRF)
           Virtual LAN: (VLAN)
           Virtual Private Network: (VPN) aka., Tunnel
           Overlay Network:
           TCP/IP Stack:
           OSI Model:
     Storage:
       Software:
         OS:
           Virtual Memory:
           Filesystem:
           Cache:
     Compute:
       Software:
         Type-1 Hypervisor: aka , VMM
         Type-2 Hypervisor:
         GuestOS:
           VM:
         OS:
           Container:
           Shell: aka , Console. Terminal
           Application:
           Job:
           Task:
           Process:
           Thread:
           Fiber:
           Context Switching:
           Driver:
           ISA:
       Hardware:
         Registers:
         L1/L2/L3 Cache:
         Pipelining:
         ABI:
         HAL:

### System Property Definitions:
Security:
  Security is a Full Stack endeavor.
  Security is the elimination or containment of threats to resources you care about. 
  What constitutes a threat?
    Any thing or anyone who wants to damage, destroy, steal, or inhibit any resource you care about.
  What constitutes a resource you care about?
    Your physical infrastructure.
    Your services and/or products.
    Your customer data.
    Your business data.
    Any noun: person, place or thing.
    etc.

Efficiency:
  Efficiency is a Full Stack endeavor.
  Efficiency is about doing more with less.
  Efficiency is all about minimizing resources while maximizing productivity.
  Efficiency decreases Capex because you have to buy fewer things;
  and also decreases Opex because there are fewer things to maintain (install, configure, etc.)
  and fewer things to power and cool;
  and by definition each item is more efficient to power and cool.

Economy of Scale:
  Economy of Scale is about doing more with more.
  Economy of Scale is a ratio of signal (what you want) to noise (what you don't want).
  For example:
    Consider a square bottle (cube) of liquid soap.
    The bottle is 1/16" thick.
    The soap is the signal, the bottle is the noise.
    A square bottle (cube) with dimensions 5"x5"x5" has an area of 6x5"^2x1/16" ~= 40cu.in. and a volume of 5^3=125cu.in. with ratio 125(signal):40(noise) ~= 3.
    A square bottle (cube) with dimensions 10"x10"x10" has an area of 6x10"^2x1/16" ~= 38cu.in. and a volume of 10^3=1000cu.in. with ratio 1000(signal):38(noise) ~= 26.
    Thus, the larger the bottle, the more soap (signal) you get per material of bottle (noise).
    In our soap example, you get approximately 26/3 ~= 8 times more soap per material of bottle for the larger bottle versus the smaller bottle.
    This is because volume grows larger than area.
  Typically, the larger something is, the more efficient it is (up to a point).
    e.g., HVAC units are more efficient the larger they are.
  Economy of Scale increases Capex because larger items cost more;
  and increases Opex because larger items use more power and cooling;
  but also decreases Opex because there are fewer things to maintain (install, configure, etc.).

Performance:
  Performance is a Full Stack endeavor.
  Performance is about maximizing speed, capacity, and efficiency.
  Throughput is speed x capacity.
  Consider a highway with a maximum speed limit (speed) and some number of lanes (capacity).
  You increase throughput and efficiency by:
  1) Increasing the speed limit (clock rate for computers).
  and/or
  2) Increasing the number of lanes (parallelism).
  and/or
  3) Removing any obstructions (bottlenecks) from the road/lanes (roadkill) and/or any obstructions (bottlenecks) inhibiting your speed.
  and/or
  4) Avoiding rush hour traffic (scheduling/concurrency).
  My highway example is a simple single level system.
  Complex systems (like computers) are non-linear/dynamic multilevel (Full Stack) systems.
  High performance equipment increases Capex because they are more expensive to buy;
  but are typically Opex neutral because maintaining high performance equipment is
  typically similar or identical to maintaining less performant equipment.
  Although high performance equipment may cost more to power and cool, thus increasing Opex.

High Availability: (HA)
  High Availability is about adding redundancy which eliminates all single points of failure.
  HA increases resiliency because the system avoids failures by eliminating single points of failure. 
  HA increases Capex because you have to buy more equipment,
  and increases Opex because there is more equipment to power, cool, and maintain
  and a more complex configuration and interactions among the equipment.
  Configuring redundancy typically falls into two categories/scenarios:
  1) Active-Active:
     All equipment is actively used.
     Capacity planning is important in this scenario.
     If you configure each item to handle full capacity, then there is no loss of performance when a failure happens, but this significantly increases Capex.
     If you configure each item to handle less than 50% capacity,
     then your system will become overloaded when a failure happens
     which may lead to less than desirable performance for your customers at best,
     and a complete failure of your system (which defeats the purpose of redundancy) at worst.
     If you configure each item to handle more than 50% capacity,
     then your performance will decrease when a failure happens,
     but your system is still fully functional.
     How much capacity you configure per item determines your customer's experience.
     Active-Active can handle higher capacity than Active-Passive for obvious reasons.
  2) Active-Passive: aka., Hot Standby
     Each item should be configured to have the same capacity,
     so when a failure happens there is no loss of service.

### The Six Pillars of Platform Engineering:
https://thenewstack.io/the-6-pillars-of-platform-engineering-part-1-security/
1) 
2) 
3) 
4) 
5) 
6) 

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
     

