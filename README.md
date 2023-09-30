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
+ Well Documented:
  
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
Complexity is incremental.
Complexity comes from dependencies and obscurity.
You have to sweat the details.
Don't let complexity creep in.

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
1) Practice these Design Priciples:
   Practice does NOT make Perfect!
   Perfect Practive makes Perfect!
   Practice!, Practice!, Practice!
   There's no substitute for doing!
   Book learning will only get you so far.
2) Design is about making tradeoffs and compromises at all levels of your System.
   e.g., Security vs. Convenience, Capex vs. Opex, etc.
   Great design includes great documentation.
   Be Strategic:
   The overall goal MUST be a great design.
   Simplifies future development.
   Don't be short sighted, have a long term vision for your success!
   Take extra time today.
   Pays back in the long run.
4) Define Clear Objectives:
5) Define How you Measure Success:
6) Efficient Communication:
   ABC = Accurate, Brief and Clear
   CCC = Correct, Concise, Clear
7) Problem Decomposition: https://en.wikipedia.org/wiki/Decomposition_(computer_science)
8) Keep it Simple Stupid: (KISS) https://en.wikipedia.org/wiki/KISS_principle
   Complexity is the enemy of clarity!
9) Separation of Concerns: (SoP) https://en.wikipedia.org/wiki/Separation_of_concerns https://en.wikipedia.org/wiki/Separation_of_content_and_presentation
10) Single Responsibility Principle: (SRP) https://en.wikipedia.org/wiki/Single_responsibility_principle
11) Principle of Least Privilege: https://en.wikipedia.org/wiki/Principle_of_least_privilege?=#- aka., (PoLP), Principle of Least Authority (PoLA)
12) Principle of Compositionality: https://en.wikipedia.org/wiki/Principle_of_compositionality
13) Abstraction: See: "Computer Abstractions"

### Computer Abstractions:
I use the terms Layers and Levels interchangably.
In other words, Layers and Levels are synonyms/equivalent.
As mentioned above "Your System is a Stack comprised of Abstract Layers".
Every layer has it's own language/vocabulary/terms/nomenclature.
Every layer produces and Emergent Higher Layer by defining an Interface.
An Interface is the location where objects interact/couple/etc.
I call the combination of all the Layers of your System the "Full Stack".
John Ousterhout, creator of the TCL Language and TCL/TK likes to ask the following question:
"What is the most important concept in Computer Science?"
He asked Donald Knuth this question and his answer was: "Layers of Abstraction".
John Ousterhout's answer to this question was: "Problem Decomposition".
https://www.youtube.com/watch?v=lgZ7Cxt5uIU#t=00h03m56s
*) Abstraction: Abstraction is hiding complexity. Abstraction is a simple interface that hides the complexity behind it. https://en.wikipedia.org/wiki/Abstraction https://en.wikipedia.org/wiki/Abstraction_(computer_science) https://en.wikipedia.org/wiki/Abstraction_layer
   Information Hiding: https://en.wikipedia.org/wiki/Information_hiding
   Encapsulation: https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)
   Modularity: https://en.wikipedia.org/wiki/Modularity https://en.wikipedia.org/wiki/Modular_design https://www.win.tue.nl/~wstomv/edu/2ip30/references/criteria_for_modularization.pdf
   Markov Blanket: https://en.wikipedia.org/wiki/Markov_blanket
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


  
### IT Industry Definitions:
What is a Data Center? 
  There are currently four data center tiers, ranked by performance and uptime.
  https://phoenixnap.com/blog/data-center-tiers-classification
  https://www.impactmybiz.com/blog/data-center-tiers-explained/
What is Platform Engineering?
  Platform Engineering ensures that there isn't an "us and them" mentality,
  which leads to a bad overall customer experience.
  Platform Engineering is all about accelerating software delivery efficiency and velocity.
  Platform Engineering gives developers the tools they want to use.
What is Site Reliability Engineering (SRE)?
  SRE is all about performance and application/system reliability.
  SRE is the practice of using software tools to automate IT infrastructure
  tasks such as system management and application monitoring.
  SRE teams use software as a tool to manage systems, solve problems, and automate operations tasks.
What is DevOps?
  DevOps is supposed to solve the problem of siloed teams blaming each other when things go wrong.
  DevOps is mainly a culture of communication and cross-functional collaboration.
  DevOps is a set of practices that emphasizes collaboration and communication
  between software developers and IT operations professionals to deliver software
  faster and more efficiently.
  DevOps helps to automate the process of software development, testing, deployment, and operations.
What is DevSecOps?
  DevSecOps is a way of approaching IT security with an "everyone is responsible for security" mindset.
  The goal of DevSecOps is to incorporate security into all stages of the software development workflow.
What is GitOps?
  GitOps is centered around using a version control system (such as Git)
  to house all information, documentation, and code for a Kubernetes deployment,
  and then use automated directors to deploy changes to the cluster.
  GitOps enables the same process developers use to merge code using pull requests
  or merge requests to be used to deploy to Kubernetes.
What is FinOps?
  
What is DORA?
  DORA stands for DevOps Research and Assessment (DORA) team.
  DORA is a team at Google who investigates the State of DevOps.
  DORA's objective is in helping organizations achieve high DevOps
  and organizational performance with data-driven insights.
  The DORA team publishes reports like:
  https://cloud.google.com/devops/state-of-devops/
  https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance
  https://cloud.google.com/blog/products/devops-sre/the-2019-accelerate-state-of-devops-elite-performance-productivity-and-scaling
What is Infrastructure as Code (IaC)?
What is Platform as a Service (PaaS)?
What is Zero Trust?
What is a Microservice Application?
What is a Monolithic Application?
What is Event Driven Architecure (EDA)?
What is a Software Development LifeCycle (SDLC)?
What is CI/CD?
What is a Software Deployment?
What is Observability?
  Observability is the ability to ask new questions of the health
  of your running services without deploying new instrumentation.
  The term comes from control theory, which defines observability
  as the ability to understand the internal state of a system from
  its external outputs (source).
What is Telemetry?
  Telemetry consists of those external "outputs" mentioned in observability.
  Telemetry is the data generated by your system that documents its state.
  Telemetry gets generated because of instrumentation:
  code or tooling that captures data about the state of your running system
  and stores it in various formats.
  Examples of software telemetry include: metrics, logs, traces, and structured events.
What is High-Cardinality Data: (HCD)
  HCD is a large set of unique values that can be queried and analyzed
  and is the most effective data when it comes to resolving an incident.
  The ability to properly analyze high-cardinality data leads to faster incident resolution.
  High-cardinality data can showcase the "where" and the "why" of a problem,
  and nothing is more effective at finding anomalies.
  To achieve true observability, leveraging high-cardinality data is a must.
  Cardinality is simply a reflection of an attribute's uniqueness.
  A user-ID, Social Security Number, Passport ID, Email Address are all
  high cardinality attributes, while geo-location is low cardinality.
  Low-cardinality data can help teams examine broad patterns in a service.
  High-cardinality data is a narrow magnifying glass into a service's problems,
  making it possible to look at outlying events that can help guide troubleshooting efforts.
What is High-Dimensionality data: (HDD)
  While high cardinality refers to a large number of data points (values) in a given attribute,
  dimensionality takes it further: how many attributes does an event have?
  Being able to analyze trends across many dimensions quickly is important
  when you're trying to figure out what changed but don't know what to ask.
  When you're trying to solve unknown-unknowns, high-dimensionality data is your friend.
What is Curse of Dimensionality:
  The curse of dimensionality refers to various phenomena that arise when
  analyzing and organizing data in high-dimensional spaces that do not
  occur in low-dimensional settings such as the three-dimensional physical
  space of everyday experience.
  The amount of data needed often grows exponentially with the dimensionality.
  In high dimensional data, all objects appear to be sparse and dissimilar in many ways,
  which prevents common data organization strategies from being efficient.

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

### On Prem Information
Introduction:
  The purpose of this section is to give a "bigpicture" view of an OnPrem Infrastructure.
  I you're going Cloud Native/Fully Managed, you don't need to know a lot of the following steps.
  The following is a description of a basic setup of an OnPrem Infrastructure:
  This is a quick, short, and incomplete list of necessities.
  I'm skipping Data Center topics like Generators, UPSes, Power Design, HVAC Cooling Design, Security,
  Peering Relationships and Negotiations, Cost Estimation, etc. because that really requires another full document to explain.
  And, I'm not a Data Center Design Engineer, eventhough I've now spent over 30+ years in Data Centers.
Pick at least 3 Data Centers: (for redundancy)
  Configure BGP Peering Connections - aka., Connect your Data Center to the Internet.
  Purchase equipment (routers, switches, servers, loadbalancers, Firewalls, etc.).
  Ship Equipment to Data Centers.
  Rack and Cable all the equipment: Power, Network, etc.
  Create and Deploy LAN Network Design: Valley-free Routing vs. Leaf and Spine Topology, LAG and/or MLAG, etc.
  Install OS or Type-1 Hypervisor on all baremetal machines with bootstrap tools: iPXE, Tinkerbell, Shoelaces, etc.
  Configure all servers with your Provisioning Tools: Ansible, Terraform, DNF/RPM, etc.
  Create VMs and/or Containers on your servers.
  Install Container Orchestration Software on baremetal or VMs: Kubernetes et.al.
  Design Kubernetes System Design to best support your workload.
  Deploy applications on Kubernetes cluster.
  Maintain everything!
  Have Fun!
  Make Money!
Aquire and Configure all non-hardware Internet Related Resources to get you up and running.
  This short list includes: 
  aquiring an ASN, CIDR Blocks, establishing BGP Peering, configure BGP Anycast, create and implement WAN design, etc.
  Again, the details of doing even this short list took me 30+ years to perfect.
ARIN:
  All resource requests require an ARIN Online account linked to either an Admin or Tech Point of Contact (POC) record
  with the authority to request resources for a valid Organization Identifier (Org ID).
  Aquire ASN from ARIN:
    https://www.arin.net/resources/guide/quickguide.pdf
    https://www.arin.net/blog/2019/09/24/how-to-request-an-asn-from-arin/
    https://ipinfo.io/<ASN>
    https://mxtoolbox.com/asn.aspx
    http://navigators.com/isp.html
    https://www.peeringdb.com/
  Aquire from ARIN IP CIDR Block/Addresses (IPv4 or IPv6) - IPv6 is preferred!
    https://www.youtube.com/watch?v=nCm6bLPh-Pw#t=00h00m00s?=#- Using Your ARIN Online Account - Requesting IP Address Space
    https://www.arin.net/resources/guide/request/
    https://www.arin.net/resources/guide/ipv4/request/
    https://www.arin.net/resources/guide/ipv6/
    https://www.arin.net/resources/guide/ipv6/first_request/
    https://www.arin.net/resources/guide/ipv6/preparing_apps_for_v6.pdf
    https://www.arin.net/reference/materials/cidr.pdf
    https://mxtoolbox.com/arin.aspx
    https://datatracker.ietf.org/doc/html/rfc4632
    http://www.cidr-report.org/as2.0
    https://bgp.potaroo.net/index-cidr.html
    https://ip2cidr.com/
    https://whoisrequest.com/
BGP: (iBGP,eBGP)
  Establish BGP peering relationship, aka., Connect your Data Center to the Internet.
BGP Tools:
  https://bgplay.massimocandela.com/
  https://github.com/massimocandela/BGPlay
  https://lookinglass.org/
  https://www.bgp4.as/looking-glasses
  https://bgpview.io/
  https://bgp.potaroo.net/index-bgp.html
  https://github.com/irrtoolset/irrtoolset
IPv4:
  RFC1918: Non-Routable IPv4 Networks/Addresses
IPv4 Tools:
  https://mxtoolbox.com/NetworkTools.aspx
  https://mxtoolbox.com/subnetcalculator.aspx
IPv6:
  RFC???: Non-Routable IPv6 Networks/Addresses
  https://mxtoolbox.com/NetworkTools.aspx
IPv6 Tools:
  http://www.ipamworldwide.com/libraries/toolmenu.html
Register Domain Names:
  There are several Domain Registrars:
  https://www.bluehost.com/domains
  https://www.godaddy.com/domains
Network Time Protocol: (NTP)
  If your time is off on your servers, then your logs will be off
  and other applications will also start to fail!
  NTP gives client synchronization accuracies in the millisecond range.
  I use NTPsec:
  $ dnf install -y ntpsec
  ftp://ftp.ntpsec.org/pub/releases/ntpsec-1.1.8.tar.gz
  https://www.ntpsec.org/
  https://docs.ntpsec.org/latest/NTS-QuickStart.html
  https://docs.ntpsec.org/latest/build.html#unix
  https://github.com/ntpsec/ntpsec
  https://github.com/ntpsec/ntpsec.github.io
  https://gitlab.com/NTPsec
  https://gitlab.com/NTPsec/ntpsec/blob/master/devel/nts.adoc
  https://weberblog.net/setting-up-nts-secured-ntp-with-ntpsec/
  $ cat /etc/ntpsec/ntp.conf
  $ hwclock --show
  $ timedatectl status
  $ ntpdate -q us.pool.ntp.org
  $ ntpdate -q 0.pool.ntp.org
  $ ntpq -p
  $ ntpq -c rv
  Computer Network Time Synchronization:
    https://www.eecis.udel.edu/~mills/book.html
  Open Time Server:
    http://www.opentimeserver.com/
    https://github.com/opencomputeproject/Time-Appliance-Project/tree/master/Open-Time-Server
  Google Public NTP:
    https://developers.google.com/time
  Cloudflare Time Services:
    time-services@cloudflare.com
    https://time.cloudflare.com/
    https://www.cloudflare.com/time/
  NIST Internet Time Servers:
    https://tf.nist.gov/tf-cgi/servers.cgi
  NTP Pool Project:
    https://www.ntppool.org/en/
Precision Time Protocol: (PPT) IEEE 1588
  PPT gives slave synchronization accuracies in the nanosecond or microsecond range.
  https://en.wikipedia.org/wiki/Precision_Time_Protocol
  https://en.wikipedia.org/wiki/IEEE_1588
  https://www.nist.gov/el/intelligent-systems-division-73500/ieee-1588
  https://linuxptp.sourceforge.net/
DNS: ISC-BIND (stable versions are even release numbers)
  Kubernetes uses CoreDNS for DNS resolution amoung their Pods.
  I use ISC-BIND for the Baremetal and VMs underneath Kubernetes.
  Public DNS: 1.1.1.1, 8.8.8.8, 8.8.4.4, 9.9.9.9
  https://www.isc.org/bind/
  https://downloads.isc.org/isc/bind9/cur/
  https://downloads.isc.org/isc/bind9/cur/9.18/doc/arm/Bv9ARM.pdf
DNSSEC:
  DNSSEC - What Is It and Why Is It Important?
  https://www.icann.org/resources/pages/dnssec-what-is-it-why-important-2019-03-05-en
  DNSSEC Basics
  https://www.internetsociety.org/deploy360/dnssec/basics/
  DNSSEC Overview
  https://www.youtube.com/watch?v=MrtsKTC3KDM#t=00h00m00s?=#- DNSSEC Overview
  DNSSec Explained
  https://www.youtube.com/watch?v=_8M_vuFcdZU#t=00h00m00s?=#- DNSSec Explained
DNS Tools:
  Stork is a dashboard for BIND 9 and Kea DHCP:
  https://gitlab.isc.org/isc-projects/stork
  $ man dig
  $ man mdig
  $ man delv
  $ nmap --script broadcast-dhcp-discover -e <nic-interface>
  https://www.isc.org/dns-tools/
  https://who.is/
  https://dnschecker.org/
  https://www.dnswatch.info/
  http://www.mavetju.org/download/dnstracer-1.9.tar.gz
DNS Root Servers:
  https://www.iana.org/domains/root/servers
  https://www.internic.net/domain/root.zone
  https://root-servers.org/
DHCP: ISC-KEA (replaces ISC-DHCP)
  https://www.isc.org/kea/
  https://gitlab.isc.org/isc-projects/kea
  https://kea.readthedocs.io/en/latest/
DHCP Tools:
  Stork is a dashboard for BIND 9 and Kea DHCP:
  https://gitlab.isc.org/isc-projects/stork
  https://www.isc.org/kea-tools/
  https://www.isc.org/dhcp-tools/ <-- ISC announced the end of maintenance for ISC DHCP as of the end of 2022 - use Kea instead!
  http://www.mavetju.org/download/dhcping-1.2.tar.gz
  http://www.mavetju.org/download/dhcpdump-1.8.tar.gz
Find your NAT IP:
  https://www.ipchicken.com/
  # curl ifconfig.me
  # tranceroute arin.net
Other Random Tools:
  https://www.internetlivestats.com/
  https://time.is/
  http://www.convertunits.com/dates/from/Jan+1,+2023/to/Sep+28,+2023
  https://thetruesize.com/

## My Favorite Hardware
TBD

### AI/ML/DL/RL and Platform Engineering
AI, especially LLMs, are designed to take in an enormous amount
of data and "learn" from it to achieve better than human results.
LLMs like ChatGPT4, Llama2, PaLM2, DALL-E3, Dolly2, and Diffusion Models
can outperform humans in tasks like Object Recognition, Analyzing X-Rays,
writing boilerplate code, and other "creative" tasks like Drawing Images.
Reinforcement Learning AI can outperform humans in any game
such as Go, Chess, and any Compter Games like Atari Breakout, and Doda2.
The potential of AI is enormous and I believe it will be used in every
aspect of every industry to some extent.
Platform Engineering is a perfect match for current AI technologies
because AI excels in learning from 
AI technologies, especially LLMs excel in PE tasks, like:
  1) Writing code in Bash, Python, YAML, and JSON.
  2) Learning from PE Data: Telemetry data, Logs, Monitoring metrics,
     Business and Customer data; Configuration files, Topologies Network data, etc.

### AI/ML/DL/RL Platform Engineering Objectives
1) Learn how to build, train and fine tune LLMs on PE data
   to assisit and hopefully outperform humans in tasks such
   as incidence response, root cause analysis, and Market predictions.
2) Continue learning AI Coding Assistants to write code in Bash, Python, YAML, JSON, etc.
   Here's a short list of AI Coding Assistants I'm currently using everyday
   to generate boilerplate code, which I review, correct and test; and also
   to generate Documentation, Code Comments, Github pull requests, Static analysis, generate SQL, etc.
   Github CopilotX, Codex, CodeWhisperer, Code Interpreter, Google Vertex AI Codey, Alphacode, BLOOM,
   Tabnine, StarCoder, Polycoder, CodeQL, InfraCopilot, Cody, WhatTheDiff, Stenography, Mintlify, Kats,
   Grit, Adrenaline, text2sql, askcodi, mutable.ai, Codeium, Readable, CodeT5 and CodeT5+, kiteco-public
   
   
### Other System Design Resources
*) ByteByteCode:


