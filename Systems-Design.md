# Systems Design

## System Properties:
### You want your System to be:

+ Secure: authentication, authorization, accounting (aaa); Zero-Trust
+ Reliable: slow to fail
+ Robust:  quick to recover from failure.
+ Highly Available: 99.999% uptime = less than 6 minutes downtime per year
+ High Performance: maximize speed/minimize latency
+ Scalable: maximize capacity/bandwidth (take advantage of Economy of Scale)
+ Maintainable: maximize "frictionless automation"
+ Cost Effective:  minimize Capex & Opex
+ Well Documented: strive for [Great Documentation](https://www.linkedin.com/pulse/great-ation-defined-daniel-smith/); [Writing Great Documentation](https://medium.com/@episod/writing-great-documentation-44d90367115a)
  
Every business has business goals.

These ***System Properties*** align with the high level business goal of ***"satisfy your customers"***.

### Your System is a Stack of [Abstract Layers](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#computer-abstractions):

* Storage/Data Layer:
* Network Layer:
* Compute Layer:
* Personnel Layer: all the departments and teams that are your business.

In order to achieve the above ***System Properties*** you have to:<br>
heir the ***"best people"***, applying the ***"best practices"***, using the ***"best technologies"***<br>
for each system property, and at each layer of your stack (I call this ***"Full Stack"*** implementation).<br>

This is a daunting task because there are so many choices available and so many different ways<br>
your system will behave depending on the choices you make for each property at each layer.<br>

The permutations of choices and behavior quickly explode combinatorally.<br>

This is just one of the causes that makes any System ***"complex"***;<br>
and why it requires a qualified ***System Designer*** to achieve these ***System Properties***.<br>
Other causes of complexity include:<br> 
&ensp;&ensp;non-linear dynamics, chaotic behavior, randomness (difficult to predict),<br>
&ensp;&ensp;a deep nesting of many layers of abstraction, etc. which are all symptoms<br>
&ensp;&ensp;of the combinatorial explosion I already mentioned.<br>
Complexity is incremental.<br>
Complexity comes from dependencies and obscurity.<br>
You have to sweat the details.<br>
Don't let complexity creep in.<br>

### So where do you begin?

It always starts with understanding your workload.<br>

You can't make the ***"best choices"*** without understanding your workload intimately and ***testing*** it thoroughly.<br>

Starting from a blank slate is different than inheriting an existing system infrastructure.<br>

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
  - How do they know the right questions to ask?
  - How do they define clear objectives?
  - How do they define and measure success?
  - How do they choose the best Platform Design, Tools and Practices for your Workload?
  - How do they choose the best UX/UI/Frontend Design, Tools and Practices for your Workload?
  - How do they choose the best Storage/Database/Data Design, Tools and Practices for your Workload?
  - How do they choose the best Network Design, Tools and Practices for your Workload?
  - How do they choose the best Compute Design, Tools and Practices for your Workload?
  - How do they choose the best Data Structures, Algorithms and Protocols for your Workload??
  - How do they choose the best Security Design, Tools and Policies/Practices for your Workload?
  - How do they choose the best Observability/Telemetry/Monitoring/Logging/Tracing/Analytics Design, Tools and Practices for your Workload?
  - How do they choose the best Testing/Benchmarking Design, Tools and Practices for your Workload?
  - How do they choose the best Programming Language, IDE, etc. to implement your Workload?
  - How do they choose the best SDLC, CI/CD, and Distributed Version Control System Tools and Practices/Workflows for your Workload?
+ How do your Architects/Designers/Programmers/Teams/Departments communicate and how often?
  - In person Meetings, Email, Mailing Lists, Chat, Slack, Mastadon, IRC; Video: Office365, MSTeams, Zoom, WebEx, GoToMeeting?
  - Every Week, Daily (15 min scrum), every Month, Never?
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
    - AWS has over [535 Cloud Services spanning 20+ Categories](https://www.antvaset.com/c/21gjdl7gz4) 
    - GCP has over [32 Cloud Services](https://cloud.google.com/products/) [spanning 7 Categories](https://www.infiflex.com/what-are-the-google-cloud-platform-services)
    - Azure has over [295 Cloud Services spanning 21 Categories](https://azure.microsoft.com/en-us/products/) 
+ What is your Disaster Recovery Plan (DRP)?
  - How often to you practice your DRP?
  - How do you Failover your workload?
  - What are your Incidence Response and Root Cause Analysis (RCA) procedures.
+ What is your Network Design?
  - Where are your High-Level Network Architecture/Design Diagrams?
  - Describes your Network: Traffic Ingress/Egress, Routers, Switches, Firewalls, Load Balancers, API Gateways, iPXE, Redfish, NTP/PPT, DNS, DHCP, BGP (eBGP,iBGP), OSPF; CDNs, Edge Networking; Failover, Redundancy, etc.
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
  - AWS EC2 VMs, OnPrem Servers/VMs/Containers, etc.
+ What Infrastructure Provisioning Tools do you use?
  - Terraform, Ansible, Nomad, Kubernetes?
+ What Programming Languages do you use?
  - Python, Go, Bash, C, C++, Java, Javascript, etc.
  - What Programming Tools and/or Frameworks do you use?
    - IDEs: VSC, Vim, Emacs
    - Distributed Version Control System: Git, Github, Gitlab
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
+ What Telemetry/Metrics do you gather?
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
+ Read the [System Design Topics](https://github.com/Paul-J-Company/Systems-Design/blob/main/README.md#system-design-topics) information below which adds more details to what we've already discussed above.
+ Read my [Kubernetes]() information for how I apply these principles to a Kubernetes Environment.

## System Design Topics:

### Design Principles
1) Practice these Design Priciples:<br>
   Practice does NOT make Perfect!<br>
   Perfect Practice makes Perfect!<br>
   Practice!, Practice!, Practice!<br>
   There's no substitute for doing!<br>
   Book learning will only get you so far.<br>
2) Design is about making tradeoffs and compromises at all levels of your System.<br>
   e.g., Security vs. Convenience, Capex vs. Opex, etc.<br>
   Great design includes great documentation.<br>
   [Teaching the art of great documentation](https://developers.googleblog.com/2020/07/teaching-art-of-great-documentation.html)<br>
   [The eight rules of good documentation](https://www.oreilly.com/content/the-eight-rules-of-good-documentation/)<br>
   [12 Best Documentation Examples (Expert Picks)](https://herothemes.com/blog/best-documentation-examples/)<br>
   [The importance of documentation](https://www.atlassian.com/work-management/knowledge-sharing/documentation/importance-of-documentation)<br>
   Be Strategic:<br>
   The overall goal MUST be a great design.<br>
   Simplifies future development.<br>
   Don't be short sighted, have a long term vision for your success!<br>
   Take extra time today.<br>
   Pays back in the long run.<br>
4) Define Clear Objectives:<br>
5) Define How you Measure Success:<br>
6) Efficient Communication:<br>
   ABC = Accurate, Brief and Clear<br>
   CCC = Correct, Concise, Clear<br>
   Rule #1: Know your audience!<br>
   Always stay calm and rational.<br>
7) [Problem Decomposition:](https://en.wikipedia.org/wiki/Decomposition_(computer_science))<br>
8) [Keep it Simple Stupid: (KISS)](https://en.wikipedia.org/wiki/KISS_principle)<br>
   Complexity is the enemy of clarity!<br>
   Simple does not always imply easy!<br>
9) [Separation of Concerns: (SoP)](https://en.wikipedia.org/wiki/Separation_of_concerns)<br>
   [Separation of Content and Presentation](https://en.wikipedia.org/wiki/Separation_of_content_and_presentation)<br>
10) [Single Responsibility Principle: (SRP)](https://en.wikipedia.org/wiki/Single_responsibility_principle)<br>
11) [Principle of Least Privilege:](https://en.wikipedia.org/wiki/Principle_of_least_privilege) aka., (PoLP), Principle of Least Authority (PoLA)<br>
12) [Principle of Compositionality:](https://en.wikipedia.org/wiki/Principle_of_compositionality)<br>
13) Abstraction:<br>
    See: "[General Abstractions](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#general-abstractions)"<br>
    See: "[Computer Abstractions](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#computer-abstractions)"<br>

### General Abstractions:
An [Abstraction](https://en.wikipedia.org/wiki/Abstraction) is hiding complexity and/or [hiding information](https://en.wikipedia.org/wiki/Information_hiding).<br>
[Abstraction in Computer Science](https://en.wikipedia.org/wiki/Abstraction_(computer_science)) is a simple interface that hides the complexity behind it.<br>
An [Abstraction Layer](https://en.wikipedia.org/wiki/Abstraction_layer) includes the following concepts:<br>
&ensp;&ensp;[Encapsulation:](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming))<br>
&ensp;&ensp;[Modularity:](https://en.wikipedia.org/wiki/Modularity)<br>
&ensp;&ensp;&ensp;&ensp;[Criteria for Modularization](https://www.win.tue.nl/~wstomv/edu/2ip30/references/criteria_for_modularization.pdf)<br>
&ensp;&ensp;&ensp;&ensp;[Modular Design](https://en.wikipedia.org/wiki/Modular_design)<br>
&ensp;&ensp;[Markov Blanket:](https://en.wikipedia.org/wiki/Markov_blanket)<br>
&ensp;&ensp;[Coupling:](https://en.wikipedia.org/wiki/Coupling_(computer_programming))<br>
&ensp;&ensp;&ensp;&ensp;[Loose Coupling](https://en.wikipedia.org/wiki/Loose_coupling)<br>
&ensp;&ensp;[Cohesion:](https://en.wikipedia.org/wiki/Cohesion_(computer_science))<br>
&ensp;&ensp;&ensp;&ensp;[Cohesion Metrics](https://www.aivosto.com/project/help/pm-oo-cohesion.html)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;A cohesive class performs one function.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;A non-cohesive class performs two or more unrelated functions.<br>

### Computer Abstractions:
Introduction:<br>
&ensp;&ensp;As mentioned above "[Your System is a Stack of Abstract Layers](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#your-system-is-a-stack-comprised-of-abstract-layers)".<br>
&ensp;&ensp;I use the terms Layers and Levels interchangably.<br>
&ensp;&ensp;In other words, Layers and Levels are synonyms/equivalent.<br>
&ensp;&ensp;Every layer has it's own [language](https://en.wikipedia.org/wiki/Category:Language)/[vocabulary](https://en.wikipedia.org/wiki/Category:Vocabulary)/[terminology](https://en.wikipedia.org/wiki/Category:Terminology)/[nomenclature](https://en.wikipedia.org/wiki/Nomenclature).<br>
&ensp;&ensp;Every layer produces and Emergent Higher Layer by defining an Interface.<br>
&ensp;&ensp;An Interface is the location where objects interact/couple/etc.<br>
&ensp;&ensp;I call the combination of all the Layers of your System the "Full Stack".<br>
&ensp;&ensp;John Ousterhout, creator of the TCL Language likes to ask the following question:<br>
&ensp;&ensp;"What is the most important concept in Computer Science?"<br>
&ensp;&ensp;He asked Donald Knuth this question and his answer was: "Layers of Abstraction".<br>
&ensp;&ensp;John Ousterhout's answer to this question was: "[Problem Decomposition](https://www.youtube.com/watch?v=lgZ7Cxt5uIU#t=00h03m56s)".<br>

There are 3 Major Types of Computer Abstraction:<br>
1. One-to-Many Abstraction:<br>
   *Appears and behaves like one thing, but is actually many things.*<br>
   Network:<br>
   &ensp;&ensp;[Load Balancer:](https://en.wikipedia.org/wiki/Load_balancing_(computing))  hardware-based and software-based<br>
   &ensp;&ensp;[API Gateway:](https://en.wikipedia.org/wiki/API_management#Gateway)<br>
   &ensp;&ensp;[1-to-Many NAT/PAT:](https://en.wikipedia.org/wiki/Network_address_translation#One-to-many_NAT)<br>
   &ensp;&ensp;[Forward Proxy:](https://en.wikipedia.org/wiki/Proxy_server#Forward_proxies)<br>
   &ensp;&ensp;[Reverse Proxy:](https://en.wikipedia.org/wiki/Reverse_proxy)<br>
   &ensp;&ensp;[HSRP](https://en.wikipedia.org/wiki/Hot_Standby_Router_Protocol)/[VRRP](https://en.wikipedia.org/wiki/Virtual_Router_Redundancy_Protocol)/[CARP:](https://en.wikipedia.org/wiki/Common_Address_Redundancy_Protocol)<br>
   &ensp;&ensp;[Link Aggregation Group (LAG)](https://en.wikipedia.org/wiki/Link_aggregation)/[Link Aggregation Control Protocol (LACP):](https://en.wikipedia.org/wiki/Link_aggregation#Link_Aggregation_Control_Protocol) aka., NIC Bonding/Teaming/Trunking/Bundling/Channeling<br>
   &ensp;&ensp;[Multi-Chassis Link Aggregation Group (MLAG):](https://en.wikipedia.org/wiki/Multi-chassis_link_aggregation_group)<br>
   Storeage:<br>
   &ensp;&ensp;[RAID:](https://en.wikipedia.org/wiki/Raid)<br>
   &ensp;&ensp;[Controlled Replication Under Scalable Hashing (CRUSH):](https://ceph.com/assets/pdfs/weil-crush-sc06.pdf)<br>
   Compute:<br>
   &ensp;&ensp;[Cluster:](https://en.wikipedia.org/wiki/Computer_cluster)<br>
2) Local-Remote Abstraction:<br>
   *Appears and behaves like a local resource, but is actually a remote resource.*<br>
   Storage:<br>
   &ensp;&ensp;[Clusterd Filesystems:](https://en.wikipedia.org/wiki/Clustered_file_system) aka., Distributed Filesystems<br>
   &ensp;&ensp;[Network File System (NFS):](https://en.wikipedia.org/wiki/Network_File_System)<br>
   &ensp;&ensp;[Samba](https://en.wikipedia.org/wiki/Samba)/[SMB/CIFS](https://en.wikipedia.org/wiki/Server_Message_Block):<br>
   Compute:<br>
   &ensp;&ensp;[Application Program Interface (API):]()<br>
3) Emulation/Simulation/Virtualization Abstraction:<br>
   Appears and behaves like one thing, but is actually another.<br>
   Network:<br>
   &ensp;&ensp;OS Implements:<br>
   &ensp;&ensp;[Virtual Routing and Forwarding: (VRF)]()<br>
   &ensp;&ensp;[Virtual LAN (VLAN):]()<br>
   &ensp;&ensp;[Virtual Private Network (VPN):]() aka., Tunnel<br>
   &ensp;&ensp;[Overlay Network:]()<br>
   &ensp;&ensp;[TCP/IP Stack:]()<br>
   &ensp;&ensp;[OSI Model:]()<br>
   Storage:<br>
   &ensp;&ensp;OS Implements:<br>
   &ensp;&ensp;[Virtual Memory:]()<br>
   &ensp;&ensp;[Filesystem:]()<br>
   &ensp;&ensp;[Cache:]()<br>
   Compute:<br>
   &ensp;&ensp;OS Implements:<br>
   &ensp;&ensp;[Virtual Machines (VMs):]()<br>
   &ensp;&ensp;&ensp;&ensp;[Type-1 Hypervisor:]() aka , VMM<br>
   &ensp;&ensp;&ensp;&ensp;[Type-2 Hypervisor:]()<br>
   &ensp;&ensp;&ensp;&ensp;[GuestOS:]() runs inside Type-1,2 Hypervisors<br>
   &ensp;&ensp;[Containers:]()<br>
   &ensp;&ensp;[Shell:]() aka , Console. Terminal<br>
   &ensp;&ensp;[Applications:]() aka., Programs<br>
   &ensp;&ensp;[Jobs:]()<br>
   &ensp;&ensp;[Tasks:]()<br>
   &ensp;&ensp;[Processes:]()<br>
   &ensp;&ensp;[Threads:]()<br>
   &ensp;&ensp;[Fibers:]()<br>
   &ensp;&ensp;[Context Switching:]()<br>
   &ensp;&ensp;[Drivers:]()<br>
   &ensp;&ensp;[Instruction Set Architecture (ISA)](https://en.wikipedia.org/wiki/Category:Instruction_set_architectures):<br>
   &ensp;&ensp;Hardware Implements:<br>
   &ensp;&ensp;&ensp;&ensp;[Registers:]()<br>
   &ensp;&ensp;&ensp;&ensp;[L1/L2/L3 Cache:]()<br>
   &ensp;&ensp;&ensp;&ensp;[Pipelining:]()<br>
   &ensp;&ensp;&ensp;&ensp;[Application Binary Interface (ABI)]():<br>
   &ensp;&ensp;&ensp;&ensp;[Hardware Abstraction Layer (HAL)]():<br>

### System Property Definitions:
Security:<br>
&ensp;&ensp;Security is a Full Stack endeavor.<br>
&ensp;&ensp;Security is the elimination or containment of threats to resources you care about.<br>
&ensp;&ensp;&ensp;&ensp;What constitutes a threat?<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Any thing or anyone who wants to damage, destroy, steal, or inhibit any resource you care about.<br>
&ensp;&ensp;&ensp;&ensp;What constitutes a resource you care about?<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Your physical infrastructure.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Your services and/or products.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Your customer data.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Your business data.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Any noun: person, place or thing.<br>

Efficiency:<br>
&ensp;&ensp;Efficiency is a Full Stack endeavor.<br>
&ensp;&ensp;Efficiency is about doing more with less.<br>
&ensp;&ensp;Efficiency is all about minimizing resources while maximizing productivity.<br>
&ensp;&ensp;Efficiency decreases Capex because you have to buy fewer things;<br>
&ensp;&ensp;and also decreases Opex because there are fewer things to maintain (install, configure, etc.)<br>
&ensp;&ensp;and fewer things to power and cool;<br>
&ensp;&ensp;and by definition each item is more efficient to power and cool.<br>

Economy of Scale:<br>
&ensp;&ensp;Economy of Scale is a Full Stack endeavor.<br>
&ensp;&ensp;Economy of Scale is about doing more with more.<br>
&ensp;&ensp;Economy of Scale is a ratio of signal (what you want) to noise (what you don't want).<br>
&ensp;&ensp;For example:<br>
&ensp;&ensp;&ensp;&ensp;Consider a square bottle (cube) of liquid soap.<br>
&ensp;&ensp;&ensp;&ensp;The bottle is 1/16" thick.<br>
&ensp;&ensp;&ensp;&ensp;The soap is the signal, the bottle is the noise.<br>
&ensp;&ensp;&ensp;&ensp;A square bottle (cube) with dimensions 5"x5"x5" has an area of 6x5"^2x1/16" ~= 40cu.in. and a volume of 5^3=125cu.in. with ratio 125(signal):40(noise) ~= 3.<br>
&ensp;&ensp;&ensp;&ensp;A square bottle (cube) with dimensions 10"x10"x10" has an area of 6x10"^2x1/16" ~= 38cu.in. and a volume of 10^3=1000cu.in. with ratio 1000(signal):38(noise) ~= 26.<br>
&ensp;&ensp;&ensp;&ensp;Thus, the larger the bottle, the more soap (signal) you get per material of bottle (noise).<br>
&ensp;&ensp;&ensp;&ensp;In our soap example, you get approximately 26/3 ~= 8 times more soap per material of bottle for the larger bottle versus the smaller bottle.<br>
&ensp;&ensp;&ensp;&ensp;This is because volume grows larger than area.<br>
&ensp;&ensp;Typically, the larger something is, the more efficient it is (up to a point).<br>
&ensp;&ensp;&ensp;&ensp;e.g., HVAC units are more efficient the larger they are.<br>
&ensp;&ensp;Economy of Scale increases Capex because larger items cost more and use more power and cooling,<br>
&ensp;&ensp;but decreases Opex because there are fewer things to maintain (install, configure, etc.).<br>

Performance:<br>
&ensp;&ensp;Performance is a Full Stack endeavor.<br>
&ensp;&ensp;Performance is about maximizing speed, capacity, and efficiency.<br>
&ensp;&ensp;Throughput is speed x capacity.<br>
&ensp;&ensp;Consider a highway with a maximum speed limit (speed) and some number of lanes (capacity).<br>
&ensp;&ensp;You increase throughput and efficiency by:<br>
&ensp;&ensp;1) Increasing the speed limit (clock rate for computers).<br>
&ensp;&ensp;and/or<br>
&ensp;&ensp;2) Increasing the number of lanes (parallelism: more cores or processors).<br>
&ensp;&ensp;and/or<br>
&ensp;&ensp;3) Removing any obstructions (bottlenecks) from the road/lanes (roadkill) inhibiting your speed.<br>
&ensp;&ensp;and/or<br>
&ensp;&ensp;4) Avoiding rush hour traffic (scheduling/concurrency).<br>
&ensp;&ensp;My highway example is a simple single level system.<br>
&ensp;&ensp;Complex systems (like computers) are non-linear/dynamic multilevel (Full Stack) systems.<br>
&ensp;&ensp;High performance equipment increases Capex because they are more expensive to buy;<br>
&ensp;&ensp;but are typically Opex neutral because maintaining high performance equipment is<br>
&ensp;&ensp;typically similar or identical to maintaining less performant equipment.<br>
&ensp;&ensp;Although high performance equipment may cost more to power and cool, thus increasing Opex.<br>

High Availability (HA):<br>
&ensp;&ensp;High Availability is a Full Stack endeavor.<br>
&ensp;&ensp;High Availability is about adding redundancy which eliminates all single points of failure.<br>
&ensp;&ensp;HA increases resiliency because the system avoids failures by eliminating single points of failure.<br>
&ensp;&ensp;HA increases Capex because you have to buy more equipment,<br>
&ensp;&ensp;and increases Opex because there is more equipment to power, cool, and maintain<br>
&ensp;&ensp;and a more complex configuration and interactions among the equipment.<br>
&ensp;&ensp;Configuring redundancy typically falls into two categories/scenarios:<br>
&ensp;&ensp;1) Active-Active:<br>
&ensp;&ensp;&ensp;&ensp;All equipment is actively used.<br>
&ensp;&ensp;&ensp;&ensp;Capacity planning is important in this scenario.<br>
&ensp;&ensp;&ensp;&ensp;If you configure each device to handle full 100% capacity,<br>
&ensp;&ensp;&ensp;&ensp;then there is no loss of performance when a failure happens,<br>
&ensp;&ensp;&ensp;&ensp;but this essentially doubles Capex.<br>
&ensp;&ensp;&ensp;&ensp;If you configure each item to handle less than 50% capacity,<br>
&ensp;&ensp;&ensp;&ensp;then your system will become overloaded when a failure happens<br>
&ensp;&ensp;&ensp;&ensp;which may lead to less than desirable performance for your customers at best,<br>
&ensp;&ensp;&ensp;&ensp;and a complete failure of your system (which defeats the purpose of redundancy) at worst.<br>
&ensp;&ensp;&ensp;&ensp;If you configure each item to handle more than 50% capacity,<br>
&ensp;&ensp;&ensp;&ensp;then your performance will decrease when a failure happens,<br>
&ensp;&ensp;&ensp;&ensp;but your system is still fully functional.<br>
&ensp;&ensp;&ensp;&ensp;How much capacity you configure per item determines your customer's experience.<br>
&ensp;&ensp;&ensp;&ensp;Active-Active can handle higher capacity than Active-Passive for obvious reasons.<br>
&ensp;&ensp;&ensp;&ensp;Another advantage of active-active is that you're always exercising both devices<br>
&ensp;&ensp;&ensp;&ensp;so you know they both work. In a hot-standby scenario the secondary device is just<br>
&ensp;&ensp;&ensp;&ensp;sitting there waiting to handle traffic, so when things failover there's a non-zero<br>
&ensp;&ensp;&ensp;&ensp;probability that the device will fail because you haven't been using it.<br>
&ensp;&ensp;&ensp;&ensp;Is the hot-standby configuration right? Is it having hardware issues?<br>
&ensp;&ensp;2) Active-Passive: aka., Hot Standby<br>
&ensp;&ensp;&ensp;&ensp;Each device should be configured to have the same capacity,<br>
&ensp;&ensp;&ensp;&ensp;so when a failure happens there is no loss of service.<br>
&ensp;&ensp;&ensp;&ensp;If you're going to configure each device at 100% capacity<br>
&ensp;&ensp;&ensp;&ensp;you might as well do an active-active configuration.<br>
&ensp;&ensp;&ensp;&ensp;In a active-passive scenario you must schedule regular failovers<br>
&ensp;&ensp;&ensp;&ensp;to verify the hot-standby device is working properly.<br>

### IT Industry Definitions/Buzzwords:
What is a Data Center?<br>
&ensp;&ensp;A Data Center is a physical building located around the world that houses your Platforms, Systems, Workloads.<br>
&ensp;&ensp;There are currently [four data center tiers](https://phoenixnap.com/blog/data-center-tiers-classification), [ranked by performance and uptime](https://www.impactmybiz.com/blog/data-center-tiers-explained/<).<br>
What is Infrastructure as Code (IaC)?<br>
&ensp;&ensp;IAC is a DevOps practice of managing infrastructure in a declarative manner using code,<br>
&ensp;&ensp;rather than manually configuring it through a graphical user interface.<br>
&ensp;&ensp;Declarative: The process of declaring your desired result and the system "learns" how to achieve it.<br>
&ensp;&ensp;Imperative: The process of explaining every step to accomplish a desired result.<br>
What is Platform as a Service (PaaS)?<br>
&ensp;&ensp;PaaS is an abstraction over infrastructure that runs applications and hosts stacks.<br>
&ensp;&ensp;PaaS supports custom workflows to enable teams to function efficiently.<br>
&ensp;&ensp;PaaS enables the introduction of new ways to build, run, and deploy apps easily.<br>
&ensp;&ensp;PaaS allows underlying technology to be swapped out with no impact on teams.<br>
What is Platform Engineering?<br>
&ensp;&ensp;Platform Engineering ensures that there isn't an "us and them" mentality,<br>
&ensp;&ensp;which leads to a bad overall customer experience.<br>
&ensp;&ensp;Platform Engineering is all about accelerating software delivery efficiency and velocity.<br>
&ensp;&ensp;Platform Engineering gives developers the tools they want to use.<br>
What is Site Reliability Engineering (SRE)?<br>
&ensp;&ensp;SRE is all about performance and application/system reliability.<br>
&ensp;&ensp;SRE is the practice of using software tools to automate IT infrastructure<br>
&ensp;&ensp;tasks such as system management and application monitoring.<br>
&ensp;&ensp;SRE teams use software as a tool to manage systems, solve problems, and automate operations tasks.<br>
What is DevOps?<br>
&ensp;&ensp;DevOps is supposed to solve the problem of siloed teams blaming each other when things go wrong.<br>
&ensp;&ensp;DevOps is mainly a culture of communication and cross-functional collaboration.<br>
&ensp;&ensp;DevOps is a set of practices that emphasizes collaboration and communication<br>
&ensp;&ensp;between software developers and IT operations professionals to deliver software<br>
&ensp;&ensp;faster and more efficiently.<br>
&ensp;&ensp;DevOps helps to automate the process of software development, testing, deployment, and operations.<br>
&ensp;&ensp;Continuous Feedback is a DevOps practice where feedback is continuously<br>
&ensp;&ensp;collected and incorporated into the development process.<br>
&ensp;&ensp;[Visualizing DevOps in Kubernetes](https://github.com/metaleapca/metaleap-devops-in-k8s/blob/main/metaleap-devops-in-k8s.pdf)<br>
What is DevSecOps? aka., SecOps<br>
&ensp;&ensp;DevSecOps is a way of approaching IT security with an "everyone is responsible for security" mindset.<br>
&ensp;&ensp;The goal of DevSecOps is to incorporate security into all stages of the software development workflow.<br>
&ensp;&ensp;Some common security practices in DevSecOps include:<br>
&ensp;&ensp;code reviews, automated security testing, secure configuration management, and threat modeling.<br>
What is DORA?<br>
&ensp;&ensp;[DORA](https://cloud.google.com/blog/products/devops-sre/the-2019-accelerate-state-of-devops-elite-performance-productivity-and-scaling) stands for DevOps Research and Assessment (DORA) team.<br>
&ensp;&ensp;DORA is a team at Google who investigates the State of DevOps.<br>
&ensp;&ensp;DORA's objective is in helping organizations achieve high DevOps<br>
&ensp;&ensp;and organizational performance with data-driven insights.<br>
&ensp;&ensp;The DORA team publishes reports like:<br>
&ensp;&ensp;[2023 State of DevOps Report](https://cloud.google.com/devops/state-of-devops/)<br>
&ensp;&ensp;[Using the Four Keys to measure your DevOps Performance](https://cloud.google.com/blog/products/devops-sre/using-the-four-keys-to-measure-your-devops-performance)<br>
&ensp;&ensp;[The Four Keys](https://github.com/dora-team/fourkeys)<br>
&ensp;&ensp;[2021 Accelerate State of DevOps report addresses burnout, team performance](https://cloud.google.com/blog/products/devops-sre/announcing-dora-2021-accelerate-state-of-devops-report)<br>
&ensp;&ensp;[Google Cloud DevOps Awards](https://cloud.google.com/awards/devops)<br>
What is GitOps?<br>
&ensp;&ensp;GitOps is centered around using a version control system (such as Git, GitLab, Github)<br>
&ensp;&ensp;to house all information, documentation, and code for a Kubernetes deployment,<br>
&ensp;&ensp;and then use automated directors to deploy changes to the cluster.<br>
&ensp;&ensp;GitOps enables the same process developers use to merge code using pull requests<br>
&ensp;&ensp;or merge requests to be used to deploy to Kubernetes.<br>
&ensp;&ensp;In a GitOps workflow the desired state of your infrastructure is<br>
&ensp;&ensp;represented by the configurations stored in a Git repository.<br>
&ensp;&ensp;This Git repository serves as the single source of truth,<br>
&ensp;&ensp;and GitOps enforces the state that the cluster should be in.<br>
&ensp;&ensp;Any changes to the cluster are made by updating the configuration files<br>
&ensp;&ensp;in the Git repository, rather than directly interacting with the cluster.<br>
&ensp;&ensp;GitOps enables an auditable and reproducible process for deployments.<br>
&ensp;&ensp;Rollbacks become as simple as reverting to a known working state in the Git history.<br>
&ensp;&ensp;The changes in the infrastructure can be seen easily in the git log.<br>
&ensp;&ensp;GitOps allows for automatic and continuous synchronization between the<br>
&ensp;&ensp;desired state in the Git repository and the actual state in the cluster,<br>
&ensp;&ensp;ensuring consistency across environments, simplifying the traditionally<br>
&ensp;&ensp;complex CI/CD pipelines, and reducing human error.<br>
&ensp;&ensp;GitOps promotes collaboration and transparency among development and operations teams.<br>
&ensp;&ensp;Changes to the cluster are transparently tracked in Git,<br>
&ensp;&ensp;making it easy for team members to understand what's happening and when.<br>
&ensp;&ensp;GitOps provides self-heal capabilities.<br>
&ensp;&ensp;If somebody changes the state of the infrastructure manually, the state<br>
&ensp;&ensp;will automatically change to reflect what is defined in the Git repository.<br>
&ensp;&ensp;This brings resilience and a cluster that will be easier to debug if there is a problem.<br>
&ensp;&ensp;In GitOps, the traditional CI/CD pipeline is "reversed".<br>
&ensp;&ensp;This is called "pull-based deployments", where the target cluster constantly<br>
&ensp;&ensp;"pulls" its desired state from the Git repository, rather than relying on a<br>
&ensp;&ensp;"push" from an external entity (e.g. a CI/CD tool like Jenkins or Github Actions).<br>
&ensp;&ensp;This "pull" approach provides a self-healing mechanism, allowing the cluster to<br>
&ensp;&ensp;autonomously converge to the desired state even if it drifts due to manual changes<br>
&ensp;&ensp;or unforeseen events.<br>
&ensp;&ensp;One of the decisions you have to make as a Platform Engineer using GitOps is<br>
&ensp;&ensp;how you structure your Git repo: repo-per-app, repo-per-team, monrepo, etc.<br>
&ensp;&ensp;I always apply the Separation of Concerns Principle and typically use repo-per-app.<br>
&ensp;&ensp;But it really depends on how your Organization works and is structured.<br>
&ensp;&ensp;Trying all methods isn't a bad idea to see which one works best.<br>
&ensp;&ensp;[Visualizing IaC with and without GitOps](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*_1T9Tx62ig3yqX26IHIoWQ.png)<br>
What is FinOps?<br>
&ensp;&ensp;FinOps is about spending your money most cost-effectively.<br>
&ensp;&ensp;Yes, this might mean spending less money, but it also might<br>
&ensp;&ensp;mean spending more money and making more money.<br>
What is a Software Development LifeCycle (SDLC)?<br>
&ensp;&ensp;[SDLC](https://phoenixnap.com/blog/wp-content/uploads/2019/05/software-development-life-cycle.jpg) is a framework that describes the stages involved in the development of software.<br>
&ensp;&ensp;The typical stages of the SDLC include:<br>
&ensp;&ensp;1) Planning:<br>
&ensp;&ensp;2) Analysis:<br>
&ensp;&ensp;3) Design:<br>
&ensp;&ensp;4) Implementation:<br>
&ensp;&ensp;5) Testing:<br>
&ensp;&ensp;6) Deployment:<br>
&ensp;&ensp;7) Maintenance:<br>
What is CI/CD?<br>
&ensp;&ensp;CI/CD stands for Continuous Integration/Continuous Delivery or Deployment.<br>
&ensp;&ensp;A CI/CD Pipeline is a series of steps that must be performed<br>
&ensp;&ensp;in order to deliver a new version of software.<br>
&ensp;&ensp;GitOps simplifies CI/CD Pipelines.<br>
What is a Software Deployment?<br>
&ensp;&ensp;Kubernetes enables easy application deployment.<br>
&ensp;&ensp;There are many types of deployment strategies.<br>
&ensp;&ensp;Here are 3 popular Deployment Strategies:<br>
&ensp;&ensp;1) Canary Deployment:<br>
&ensp;&ensp;&ensp;&ensp;A technique for rolling out new features or changes to a small subset<br>
&ensp;&ensp;&ensp;&ensp;of users or servers before releasing the update to the entire system.<br>
&ensp;&ensp;&ensp;&ensp;A Canary deployment strategy is used for applications that require frequent updates.<br>
&ensp;&ensp;2) Rolling Deployment:<br>
&ensp;&ensp;&ensp;&ensp;A strategy for updating and deploying new versions of software in a controlled and gradual manner.<br>
&ensp;&ensp;&ensp;&ensp;Instead of deploying updates all at once,<br>
&ensp;&ensp;&ensp;&ensp;a rolling deployment rolls out changes incrementally,<br>
&ensp;&ensp;&ensp;&ensp;reducing the risk of downtime and allowing for easy rollbacks in case of errors.<br>
&ensp;&ensp;&ensp;&ensp;A Rolling deployment strategy is ideal for applications that require zero downtime during deployment.<br>
&ensp;&ensp;3) Blue-Green Deployment:<br>
&ensp;&ensp;&ensp;&ensp;Involves running two identical environments,<br>
&ensp;&ensp;&ensp;&ensp;one serving as the active production environment (blue)<br>
&ensp;&ensp;&ensp;&ensp;and the other as a new release candidate (green).<br>
&ensp;&ensp;&ensp;&ensp;The new release candidate is thoroughly tested<br>
&ensp;&ensp;&ensp;&ensp;before being switched with the production environment,<br>
&ensp;&ensp;&ensp;&ensp;allowing for a smooth transition without any downtime or errors.<br>
What is a Polystore?<br>
&ensp;&ensp;A polystore is the combining of different database technologies tailored for specific use cases,<br>
&ensp;&ensp;enabling organizations to optimize performance, scalability, and analytical capabilities throughout their infrastructure.<br>
&ensp;&ensp;Polystores embrace a hybrid approach, leveraging the strengths of different database technologies tailored to specific use cases.<br>
What is Serverless?<br>
&ensp;&ensp;The purpose of serverless technology is to provide a way<br>
&ensp;&ensp;to build and run applications without having to consider<br>
&ensp;&ensp;the underlying hosts at all.<br>
&ensp;&ensp;To support serverless applications, a cloud provider provisions<br>
&ensp;&ensp;and deallocates servers as needed behind the scenes.<br>
&ensp;&ensp;Containers and serverless can work together.<br>
&ensp;&ensp;For instance, the core of your application may run on containers,<br>
&ensp;&ensp;but some supplementary backend tasks, such as user authentication,<br>
&ensp;&ensp;may run on serverless functions.<br>
What is a Microservice Application?<br>
&ensp;&ensp;The term microservice is not a well-defined term.<br>
&ensp;&ensp;There is no rigorous/unambiguous definition of when a service starts or stops being a microservice.<br>
&ensp;&ensp;In general, a microservice is an architectural pattern that arranges an application<br>
&ensp;&ensp;as a collection of loosely-coupled, fine-grained services, communicating through lightweight protocols.<br>
&ensp;&ensp;The key attribute is microservices need to be independent of one another (loosely-coupled).<br>
&ensp;&ensp;Microservices run on multiple computers and communicate with each other via networked connections.<br>
&ensp;&ensp;Transactions add complexity to running microservice architectures, compared to a monolith.<br>
&ensp;&ensp;In workloads that cannot run concurrently across the network, monoliths may deliver better performance.<br>
&ensp;&ensp;The main advantages of microservices are that you can scale them horizontally and you can deploy them<br>
&ensp;&ensp;independently, so each team can deploy in parallel, accelerating the deployment process.<br>
&ensp;&ensp;The other advantage is each team can use the programming language that best suits the service.<br>
What is a Monolithic Application?<br>
&ensp;&ensp;An application is made up of services.<br>
&ensp;&ensp;A monolithic application all services run on one process/threads (memory space) on one server.<br>
&ensp;&ensp;The communication amoung services is done via Interprocess Communication (IPC) channels.<br>
&ensp;&ensp;In contrast, microservices communicate via Network Interface Cards (NICs) which are much slower.<br>
&ensp;&ensp;If your workload requires fast service communication, then a monolith may deliver better performance.<br>
What is Event Driven Architecure (EDA)?<br>
&ensp;&ensp;EDAs are composed of loosely-coupled distributed services connected by asynchronous events.<br>
&ensp;&ensp;EDAs are a way of designing and building systems that are based on the exchange of events.<br>
&ensp;&ensp;Events are notifications of some change in state or data,<br>
&ensp;&ensp;and they are typically published by one component and consumed by another in real time.<br>
What is Zero Trust?<br>
&ensp;&ensp;Zero Trust security is an IT security model that requires strict identity verification<br>
&ensp;&ensp;for every person and device trying to access resources on a private network,<br>
&ensp;&ensp;regardless of whether they are sitting within or outside of the network perimeter.<br>
What is OWASP?<br>
&ensp;&ensp;Open Web Application Security Project: (OWASP)<br>
&ensp;&ensp;OWASP is a community initiative focused on improving web application security<br>
&ensp;&ensp;through providing open-source methodologies, tools, and techniques.<br>
What is CASB?<br>
&ensp;&ensp;Cloud Access Security Broker: (CASB)<br>
&ensp;&ensp;CASB acts as a bridge between an organization's<br>
&ensp;&ensp;on-premises infrastructure and the cloud services it employs.<br>
&ensp;&ensp;The primary focus of CASB is to ensure that sensitive data<br>
&ensp;&ensp;remains secure and compliant while employees access cloud-based resources.<br>
What is SASE?<br>
&ensp;&ensp;Secure Access Service Edge: (SASE)<br>
&ensp;&ensp;SASE provides a holistic approach to networking and security in a cloud-native environment.<br>
&ensp;&ensp;SASE is an architectural framework that merges wide-area networking (WAN) capabilities<br>
&ensp;&ensp;with security functions, all delivered as a cloud-based service.<br>
What is CNAPP?<br>
&ensp;&ensp;Cloud Native APplication Protection: (CNAPP)<br>
&ensp;&ensp;A CNAPP is a holistic security solution that provides<br>
&ensp;&ensp;all the key features organizations need to secure cloud<br>
&ensp;&ensp;workloads across all life cycle stages.<br>
&ensp;&ensp;CNAPPs offer a variety of important advantages compared to disparate,<br>
&ensp;&ensp;siloed collections of cloud security tools.<br>
&ensp;&ensp;CNAPPs typically cover:<br>
&ensp;&ensp;&ensp;&ensp;1) CI/CD security management.<br>
&ensp;&ensp;&ensp;&ensp;2) Security testing and scanning of application binaries and container images.<br>
&ensp;&ensp;&ensp;&ensp;3) Managing risks associated with cloud service configuration.<br>
&ensp;&ensp;&ensp;&ensp;4) Managing cloud user identities and permissions.<br>
&ensp;&ensp;&ensp;&ensp;5) API security.<br>
&ensp;&ensp;&ensp;&ensp;6) Data security.<br>
What is Observability?<br>
&ensp;&ensp;Observability is about recording, organizing and visualizing data.<br>
&ensp;&ensp;Observability is the ability to ask new questions of the health<br>
&ensp;&ensp;of your running services without deploying new instrumentation.<br>
&ensp;&ensp;The term comes from control theory, which defines observability<br>
&ensp;&ensp;as the ability to understand the internal state of a system from<br>
&ensp;&ensp;its external outputs (source).<br>
&ensp;&ensp;Observability vs. Monitoring:<br>
&ensp;&ensp;Observability helps you get closer and closer to the root cause of an issue;<br>
&ensp;&ensp;showing you what components were involved.<br>
&ensp;&ensp;Monitoring just lets you known something's wrong.<br>
What is Telemetry?<br>
&ensp;&ensp;Telemetry consists of those external "outputs" mentioned in observability.<br>
&ensp;&ensp;Telemetry is the data generated by your system that documents its state.<br>
&ensp;&ensp;Telemetry gets generated because of instrumentation:<br>
&ensp;&ensp;code or tooling that captures data about the state of your running system<br>
&ensp;&ensp;and stores it in various formats.<br>
&ensp;&ensp;Telemetry refers to data emitted from a system, about its behavior.<br>
&ensp;&ensp;Examples of software telemetry include: metrics, logs, traces, and structured events.<br>
What is OpenTelemetry?<br>
&ensp;&ensp;OpenTelemetry is an industry-standard.<br>
&ensp;&ensp;OpenTelemetry is a vendor-neutral open-source Observability framework<br>
&ensp;&ensp;for instrumenting, generating, collecting, and exporting telemetry data<br>
&ensp;&ensp;such as (traces, metrics, logs).<br>
&ensp;&ensp;OpenTelemetry is the mechanism by which application<br>
&ensp;&ensp;code is instrumented, to help make a system observable.<br>
&ensp;&ensp;OpenTelemetry is natively supported by a number of vendors.<br>
&ensp;&ensp;[List of Vendors that support OpenTelemetry:](https://opentelemetry.io/ecosystem/vendors/)<br>
&ensp;&ensp;Cloud Observability, Grafana Labs, Jaeger, SigNoz, AppDynamics, etc.<br>
What is High-Cardinality Data (HCD):<br>
&ensp;&ensp;HCD is a large set of unique values that can be queried and analyzed<br>
&ensp;&ensp;and is the most effective data when it comes to resolving an incident.<br>
&ensp;&ensp;The ability to properly analyze high-cardinality data leads to faster incident resolution.<br>
&ensp;&ensp;High-cardinality data can showcase the "where" and the "why" of a problem,<br>
&ensp;&ensp;and nothing is more effective at finding anomalies.<br>
&ensp;&ensp;To achieve true observability, leveraging high-cardinality data is a must.<br>
&ensp;&ensp;Cardinality is simply a reflection of an attribute's uniqueness.<br>
&ensp;&ensp;A user-ID, Social Security Number, Passport ID, Email Address are all<br>
&ensp;&ensp;high cardinality attributes, while geo-location is low cardinality.<br>
&ensp;&ensp;Low-cardinality data can help teams examine broad patterns in a service.<br>
&ensp;&ensp;High-cardinality data is a narrow magnifying glass into a service's problems,<br>
&ensp;&ensp;making it possible to look at outlying events that can help guide troubleshooting efforts.<br>
What is High-Dimensionality Data (HDD):<br>
&ensp;&ensp;While high cardinality refers to a large number of data points (values) in a given attribute,<br>
&ensp;&ensp;dimensionality takes it further: how many attributes does an event have?<br>
&ensp;&ensp;Being able to analyze trends across many dimensions quickly is important<br>
&ensp;&ensp;when you're trying to figure out what changed but don't know what to ask.<br>
&ensp;&ensp;When you're trying to solve unknown-unknowns, high-dimensionality data is your friend.<br>
What is Curse of Dimensionality:<br>
&ensp;&ensp;The curse of dimensionality refers to various phenomena that arise when<br>
&ensp;&ensp;analyzing and organizing data in high-dimensional spaces that do not<br>
&ensp;&ensp;occur in low-dimensional settings such as the three-dimensional physical<br>
&ensp;&ensp;space of everyday experience.<br>
&ensp;&ensp;The amount of data needed often grows exponentially with the dimensionality.<br>
&ensp;&ensp;In high dimensional data, all objects appear to be sparse and dissimilar in many ways,<br>
&ensp;&ensp;which prevents common data organization strategies from being efficient.<br>

### The Six Pillars of Platform Engineering:
https://thenewstack.io/author/michael-fonseca/
1) Security: https://thenewstack.io/the-6-pillars-of-platform-engineering-part-1-security/
2) Pipeline: (VCS, CI/CD) https://thenewstack.io/the-6-pillars-of-platform-engineering-part-2-ci-cd-vcs-pipeline/
3) Provisioning: https://thenewstack.io/the-pillars-of-platform-engineering-part-3-provisioning/
4) Connectivity: https://thenewstack.io/the-pillars-of-platform-engineering-part-4-connectivity/
5) Orchestration: https://thenewstack.io/the-pillars-of-platform-engineering-part-5-orchestration/
6) Observability: https://thenewstack.io/the-pillars-of-platform-engineering-part-6-observability/

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

### AI/ML/DL/RL and Platform Engineering
AI, especially LLMs, are designed to take in an enormous amount
of data and "learn" from it to achieve better than human results.
LLMs like ChatGPT4, Llama2, PaLM2, DALL-E3, Dolly2, and Diffusion Models
can outperform humans in tasks like Object Recognition, Analyzing X-Rays,
writing boilerplate code, and other "creative" tasks like Drawing Images.
LLMs learn to focus on the data that matters and filters out the noise.
LLMs can turn massive amounts of unstructured information into structured data that people can act on.
LLMs can be trained to automatically create tickets in your ticketing system
and initiate the next actions in a workflow spurred by an incident or other IT event.
Reinforcement Learning AI can outperform humans in any game
such as Go, Chess, and any Compter Games like Atari Breakout, and Doda2.
The potential of AI is enormous and I believe it will be used in every
aspect of every industry to some extent.
Platform Engineering is a perfect match for current AI technologies
because AI excels in learning from large amounts of data.
AI technologies, especially LLMs excel in Platform Engineering tasks, like:
  1) Writing code in Bash, Python, YAML, and JSON.
  2) Learning from Platform Engineering Data:
     Telemetry data, Logs, , Business and Customer data;
     Configuration files, Network Topology data, etc.

### HOWTO: Use AI/ML/DL to Improve the Speed, Accuracy and Clarity of your Platform
See: AI-ML-DL-in-Platform-Engineering
1) Use LLMs to Write Boilerplate Code: This accelerates the code writing experience.
   AI Coding Assistants to write code in Bash, Python, YAML, JSON, etc.
2) Use LLMs to Learn from Telemetry Data: Log data, Monitoring data, Analytics data, Trace data, Network Topology data, etc.
   This helps predict future possible outages, find errors, and accelerates incidence response and root cause analysis.
3) Use LLMs to Learn from Business Data: This helps minimize CapEx and Opex.
4) Use LLMs to Learn from Customer Data: This helps your customers become more product and leads to a higher level of customer satisfaction.
   
### My AI/ML/DL/RL Platform Engineering Objectives
1) Learn how to build, train and fine tune LLMs on Platform Engineering data
   to assisit and hopefully outperform humans in tasks such
   as incidence response, root cause analysis, and Market predictions.
   I'm using LangChain to develop my LLMs.
3) Continue learning AI Coding Assistants to write code in Bash, Python, YAML, JSON, etc.
   Here's a short list of AI Coding Assistants I'm currently using everyday
   to generate boilerplate code, which I review, correct and test; and also
   to generate Documentation, Code Comments, Github pull requests, Static analysis, generate SQL, etc.
   Github CopilotX, Codex, CodeWhisperer, Code Interpreter, Google Vertex AI Codey, Alphacode, BLOOM,
   Tabnine, StarCoder, Polycoder, CodeQL, InfraCopilot, Cody, WhatTheDiff, Stenography, Mintlify, Kats,
   Grit, Adrenaline, text2sql, askcodi, mutable.ai, Codeium, Readable, CodeT5 and CodeT5+, kiteco-public
   
### On Prem Information
Introduction:
  The purpose of this section is to give a "bigpicture" view of an OnPrem Infrastructure.
  ***I you're going Cloud Native/Fully Managed, you don't need to know a lot of the following steps.***
  The following is a description of a basic setup of an OnPrem Infrastructure:
  This is a quick, short, and incomplete list of necessities.
  I'm skipping Data Center topics like Generators, UPSes, Power Design, HVAC Cooling Design, Security,
  Peering Relationships and Negotiations, Cost Estimation, etc. because that really requires another full document to explain.
  And, I'm not a Data Center Design Engineer, eventhough I've now spent over 30+ years in Data Centers.
  Data Center Design Engineering is a complete field on to itself.
Pick at least 3 Data Centers: (for redundancy)
  Configure BGP Peering Connections on your Border Routers - aka., Connect your Data Center to the Internet and other Data Centers.
  Purchase equipment (routers, switches, servers, loadbalancers, Firewalls, etc.).
  Ship Equipment to Data Centers.
  Rack and Cable all the equipment: Power, Network, Out-of-band Access: IPMI: Dell iDRAC, HP iLO, etc.
  Create and Deploy LAN Network Design: Valley-free Routing vs. Leaf and Spine Topology, LAG and/or MLAG, etc.
  Install OS or Type-1 Hypervisor on all baremetal machines with bootstrap tools: iPXE, ipmitool, Tinkerbell, Shoelaces, Redfish, etc.
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
  Network Engineering is a complete field on to itself.
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
  Implement your WAN Design to connect all your Datacenters together.
  Configure BGP Anycast to connect your customers to all of your Data Centers.
  For static data, use Edge Networking or CDNs to improve latency for your customers.
  For dynamic data, include a Caching layer to improve latency for your customers.
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
  Display arp cache: aka., MAC Addresses
  # arp -a
  Display IP Addressess:
  # ip a | grep inet | grep -v inet6 | grep -v 127.0.0.0
  Display Routing Table and Default Gateway
  # ip r
  Display open TCP and UDP Ports on your host
  # nmap -sU <ip-address>
  # nmap -Pn <ip-address>
IPv6:
  IPv6 has two Internal address types:
  1) Link Local: 
     Link local addresses are not routed on the Internal network or the Internet.
     Link local addresses start with fe80
     Link Local addresses are self assigned i.e. they do not require a DHCP server.
     A link local address is required on every IP6 interface even if no routing is present.
  2) Unique Local: 
     Unique Local addresses are meant to be used inside an internal network.
     Unique Local addresses are equivalent to RFC1918 addresses.
     The address space is divided into two /8 spaces: fc00::/8 for globally assigned addressing, and fd00::/8 for locally assigned addressing.
  RFC4193: Unique Local IPv6 Unicast Addresses
  https://datatracker.ietf.org/doc/html/rfc4193
  https://www.ripe.net/manage-ips-and-asns/ipv6/ipv6-address-types/ipv6addresstypes.pdf
  IPv4/IPv6 dual-stack
  https://kubernetes.io/docs/concepts/services-networking/dual-stack/
  Validate IPv4/IPv6 dual-stack
  https://kubernetes.io/docs/tasks/network/validate-dual-stack/
  Tutorial: Assigning IPv6 addresses to Kubernetes Pods and services
  https://docs.aws.amazon.com/eks/latest/userguide/cni-ipv6.html
  What the Arrival of IPv6 Support in Kubernetes Means for You
  https://deploy.equinix.com/blog/kubernetes-ipv6-ipv4-dual-stack-networking/
  https://mxtoolbox.com/NetworkTools.aspx
IPv6 Tools:
  http://www.ipamworldwide.com/libraries/toolmenu.html
Register Domain Names:
  There are several Domain Registrars:
  https://www.bluehost.com/domains
  https://www.godaddy.com/domains
Install and Configure certbot (aka., LetsEncrypt)
  Let's Encrypt is a global Certificate Authority (CA).
  Certbot lets people and organizations around the world
  obtain, renew, and manage SSL/TLS certificates.
  Certbot certificates can be used by websites to enable secure HTTPS connections.
  Certbot certifactes are free!
  https://letsencrypt.org/docs/faq/
  https://letsencrypt.org/getting-started/
  https://github.com/letsencrypt/website/
  https://letsencrypt.org/documents/isrg-cps-v3.0/
  https://letsencrypt.org/docs/client-options/
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
Configure Out-of-band Access to all Servers:
  IPMI: Dell iDRAC, HP iLO, etc.
  # dnf install ipmitool ipmiutil
  Discover all ipmi servers on your network:
  # ipmiutil discover
Find your NAT IP:
  https://www.ipchicken.com/
  # curl ifconfig.me
  # tranceroute arin.net
Other Random Tools:
  https://www.google.com/intl/en/ipv6/statistics.html
  https://time.is/
  http://www.convertunits.com/dates/from/Jan+1,+2023/to/Sep+28,+2023
  https://thetruesize.com/

## My Favorite Hardware/Software for OnPrem Compute and Storage
Network Hardware:
  NOTE:
    I'm not including Load Balancers or Firewalls because I prefer
    using the built-in security features of Kubernetes and all of
    the Kubernetes 3rd party options for securing a cluster.
  Routers:
    Juniper:
      I prefer JunOS over Cisco IOS.
      https://www.juniper.net/us/en/products/routers.html
    Cisco:
      https://www.cisco.com/c/en/us/products/routers/product-listing.html
      https://www.cisco.com/c/en_my/products/routers/index.html
    FRR:
      An inexpensive alternative would be to use a powerful Linux server with 100Gb NICs and FRR software.
      The only issue is FRR doesn't support MLAG which is a critical protocol for configuring redundancy.
      https://en.wikipedia.org/wiki/FRRouting
      https://github.com/FRRouting/frr
      https://frrouting.org/
      https://docs.frrouting.org/en/stable-9.0/
  Switches:
    Edgecore
      https://www.edge-core.com/productsList.php?cls=291&cls2=327
    100Gb Switches
      https://www.edge-core.com/productsList.php?cls=1&cls2=5
    AS7816-64X: 64 ports 100G QSFP28 
      https://www.edge-core.com/productsInfo.php?cls=1&cls2=5&cls3=166&id=309
    AS7726-32X: 32 ports 100G QSFP28, 2 x 10G SFP
      https://www.edge-core.com/productsInfo.php?cls=&cls2=&cls3=15&id=545
    Edgecore AS5912-54X: 48 ports 10G + 6 ports 100G 
      https://www.edge-core.com/productsInfo.php?cls=291&cls2=327&cls3=328&id=264
  Fiber NICs:
    10Gb SFP+ PCI-E Network Card NIC, with Broadcom BCM57810S Chip, Dual SFP+ Port, PCI Express X8
      https://www.amazon.com/Ethernet-Broadcom-BCM57810S-Controller-Interface/dp/B06X9T683K?th=1
    100GbE Intel Ethernet Network Adapter E810
      https://www.intel.com/content/www/us/en/products/details/ethernet/800-network-adapters/e810-network-adapters/products.html
      https://www.intel.com/content/www/us/en/content-details/787658/deliver-high-performance-networking-on-ethernet.html
Baremetal Servers:
  SuperStorage SSG-136R-NEL32JBF:
  https://www.supermicro.com/en/products/system/1U/136/SSG-136R-NEL32JBF.cfm
    32 Hot-swap NVMe, 9.5mm EDSFF Long SSDs
    https://www.supermicro.com/en/products/nvme
  Fujisu RX2540M7:
  https://www.fujitsu.com/global/products/computing/servers/primergy/rack/rx2540m7/index.html
    2RU, dual-socket server with
    up to 60 Xeon cores per CPU,
    up to 8TB of DDR5 memory,
    PCIe gen 5 connectivity,
    up to 6x Nvidia GPUs,
    up to 24x 2.5-inch NVMe storage drives,
    and optionally six more at the rear of the chassis.
Storage Devices: SSDs, HDDs
  I/O Bandwidth Doubles every 3 years - BUT latency lags behind "Memory Wall" "Von Neumann Bottleneck"
  PCIe 6.0  128 GB/s (PAM4)
  PCIe 5.0   64 GB/s (NRZ)
  PCIe 4.0   32 GB/s (2 GB/s/lane)
  PCIe 3.0   16 GB/s (1 GB/s/lane)
  1) E1.L (Long) NVMe SSDs
     https://www.intel.com/content/www/us/en/products/docs/memory-storage/solid-state-drives/edsff-brief.html
  2) Ultrastar DC HC670
     https://www.westerndigital.com/products/internal-drives/data-center-drives/ultrastar-dc-hc670-hdd#ultrastar-dc-hc670-26-tb
     26TB, 7200 RPM, 261MB/s
Storage Software:
  1) Ceph:
     Supports object, block, and filesystem storage
     https://github.com/ceph/ceph
     https://ceph.com/
     https://github.com/ceph/ceph-csi
  2) Linstor: high performance block storage
     https://github.com/piraeusdatastore/linstor-csi
     https://linbit.com/linstor/
  3) OpenEBS: aka., Maystor, based on SPDK
     Perfect for a database farm in Kubernetes.
     https://spdk.io/
     https://github.com/openebs/cstor-csi
     https://github.com/openebs/mayastor
     https://openebs.io/docs/concepts/mayastor
     https://mayastor.gitbook.io/introduction/
     https://percona.community/blog/2020/10/23/mayastor-lightning-fast-storage-for-kubernetes/
     https://blocksandfiles.com/2021/03/08/intel-says-mayastor-is-fastest-open-source-storage/
  4) RAMCloud: great for streaming applications; very specialized; trying to get it to work with Kubernetes
     https://github.com/PlatformLab/RAMCloud
     https://ramcloud.atlassian.net/wiki/spaces/RAM/overview
     https://ramcloud.atlassian.net/wiki/spaces/RAM/pages/6848537/Deciding+Whether+to+Use+RAMCloud
     https://web.stanford.edu/~ouster/cgi-bin/papers/ramcloud-tocs.pdf
     To achieve low latency, RAMCloud stores all data in DRAM at all times.

### Other System Design Resources
*) ByteByteCode:
   https://www.youtube.com/@ByteByteGo/videos
   Data Replication: A Key Component for Building Large-Scale Distributed Systems
   https://blog.bytebytego.com/p/data-replication-a-key-component
   The Most Beloved Burger for Developers
   https://www.youtube.com/watch?v=7swoLEqABhQ
   10+ Key Memory & Storage Systems: Crash Course System Design #5
   https://www.youtube.com/watch?v=lX4CrbXMsNQ
   10 Key Data Structures We Use Every Day
   https://www.youtube.com/watch?v=ouipSd_5ivQ
   Top 7 Most-Used Distributed System Patterns
   https://www.youtube.com/watch?v=nH4qjmP2KEE
   Latency Numbers Programmer Should Know
   https://www.youtube.com/watch?v=FqR5vESuKe0
   What Are Microservices Really All About? (And When Not To Use It)
   https://www.youtube.com/watch?v=lTAcCNbJ7KE
   Kubernetes Explained in 6 Minutes
   https://www.youtube.com/watch?v=TlHvYWVUZyc
   CI/CD In 5 Minutes
   https://www.youtube.com/watch?v=42UP1fxi2SY
   8 Key Data Structures That Power Modern Databases
   https://www.youtube.com/watch?v=W_v05d_2RTo

*) Be A Better Dev:
   https://www.youtube.com/@BeABetterDev/videos
   Intro to AWS - The Most Important Services To Learn
   https://www.youtube.com/watch?v=FDEpdNdFglI
   Real Life AWS Project Architectures
   https://www.youtube.com/watch?v=_W1xlhDsiAE
   Introduction to AWS | A Complete Beginner Roadmap
   https://www.youtube.com/watch?v=lTyqzyk86f8
   












