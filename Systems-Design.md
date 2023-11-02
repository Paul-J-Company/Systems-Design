# Systems Design

## Systems Design Table of Contents (ToC)
+ Start by reading [Systems Properties](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#systems-properties) - this page.
+ Then read my [Systems Design Topics](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Topics.md) information that adds more details to what we've already discussed here.
+ Then read my [Systems Design Kubernetes](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Kubernetes.md) information for how I apply these principles to a Kubernetes Environment.
+ Then read my [Systems Design AI](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-AI.md) information for how AI helps in System Design.
+ Then read my [Systems Design OnPrem](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-OnPrem.md) information for how to setup an OnPrem Infrastructure.
+ Then read my [Theory and Concepts that will make you a better Systems Designer](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Theory-and-Concepts.md) information for how theory helps in Systems Design.

## Systems Properties:
### You want your System to be:

+ Secure: authentication, authorization, accounting (aaa); Zero-Trust
+ Reliable: slow to fail
+ Robust:  quick to recover from failure.
+ Highly Available: 99.999% uptime = less than 6 minutes downtime per year
+ High Performance: maximize speed/minimize latency
+ Scalable: maximize capacity/bandwidth (take advantage of Economy of Scale)
+ Maintainable:<br>
  - Maximize "[frictionless automation](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Topics.md#three-levels-of-maturity-for-infrastructure-automation)".<br>
  - Easy to Install, Configure, Use and Upgrade.<br>
  - Simple: easy to learn and understand.<br>
  - Sustainable: the capacity to maintain or improve the state and availability of something desirable.<br>
  - Predictable: no surprises or unforseen side-e-effects.<br>
  - Flexible: easy to change and adapt; Extensible: easy to add features.<br>
+ Cost Effective: minimize Capex & Opex
+ Well Documented: strive for [Great Documentation](https://www.linkedin.com/pulse/great-ation-defined-daniel-smith/); [Writing Great Documentation](https://medium.com/@episod/writing-great-documentation-44d90367115a)
+ Aligned with Business Objectes: the reason your business exists 
  - Every business has Business Objectives.
  - These ***System Properties*** align with the high level business objective of ***"satisfy your internal and external customers"***.

### Your System is a [Stack](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*NsNFTKROicAKdw1z.png) of [Distributed](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing) [Abstract Layers](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Theory-and-Concepts.md#computer-abstractions):

* Storage/Data Layer:
* Network Layer:
* Compute Layer:
* Personnel Layer: all the departments and teams that are your business.

In order to achieve the above ***System Properties*** you have to:<br>
heir the ***"best people"***, applying the ***"best practices"***, using the ***"best technologies"***<br>
for each [system property](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#system-properties), and at each [layer of your stack](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#your-system-is-a-stack-of-abstract-layers) (I call this a ***"Full Stack"*** endeaver).<br>

This is a daunting task because there are so many choices available and so many different ways<br>
your system will behave depending on the choices you make for each [system property](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#system-properties) at each [layer of your stack](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#your-system-is-a-stack-of-distributed-abstract-layers).<br>

The permutations of choices and behavior quickly [explode combinatorally](https://en.wikipedia.org/wiki/Combinatorial_explosion).<br>

This is just one of the causes that makes any System ***"complex"***;<br>
and why it requires a qualified [***System Designer***](https://www.linkedin.com/in/paul-company-7229011/) to achieve these [***System Properties***](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#system-properties).<br>
Other causes of complexity include:<br>
&ensp;&ensp;[Fallacies of Distributed Computing](https://en.wikipedia.org/wiki/Fallacies_of_distributed_computing)<br>
&ensp;&ensp;non-linear dynamics, chaotic behavior, randomness (difficult to predict),<br>
&ensp;&ensp;a deep nesting of many layers of abstraction which all contribute<br>
&ensp;&ensp;to the [combinatorial explosion](https://en.wikipedia.org/wiki/Combinatorial_explosion) I already mentioned.<br>
Complexity is incremental.<br>
Complexity comes from dependencies and obscurity.<br>
You have to sweat the details.<br>
Don't let complexity creep in.<br>

### So where do you begin?

It always starts with understanding your [workload](https://en.wikipedia.org/wiki/Workload).<br>
Your [workload](https://en.wikipedia.org/wiki/Workload) is the main application your customers interact with (aka., your "Product and/or Service").<br>
You can't make the ***"best choices"*** without understanding your [workload](https://en.wikipedia.org/wiki/Workload) intimately and ***testing*** it thoroughly.<br>
Starting from a blank slate is different than inheriting an existing system infrastructure.<br>

### Here are some System Design questions to get you started:

### System Design Questions:
+ Definitions:
  - Infrastructure: The physical resources that support your environment, includes: Data Centers, Platforms, Systems, Workloads, People.
  - Data Center: A Physical Building located around the world that houses your Platforms, Systems, Workloads.
  - Platform: The logical term that supports your environment: OnPrem, Cloud-Based, Cloud Native, Multi-Cloud, Hybrid Cloud; Private Cloud, Public Cloud
  - System: the collection of components (hardware,software,people) that interact together to implement your Platform.
  - [Workload:](https://en.wikipedia.org/wiki/Workload) the main application your customers interact with (aka., your "Product and/or Service").
  - People: all your employess across all of your departments: Platform Engineers/SREs/DevOps/DevSecOps/Programmers; Sales, Marketing
  - [High-Level](https://en.wikipedia.org/wiki/High-level_design) typically means [Grand Scheme](https://en.wiktionary.org/wiki/grand_scheme#English) and is sometimes referred to as [The Big Picture](https://www.linkedin.com/pulse/its-30000-foot-view-objective-big-picture-luis-a-ramirez-mba-mir/) or [The 30,000-foot view](https://nanoglobals.com/glossary/30000-foot-view/).
+ How do you make decisions regarding all of the questions below?
  - Who are your Architects/Designers?
  - Where are their [High-Level](https://en.wikipedia.org/wiki/High-level_design) Architecture/Design Diagrams?
  - How do they strike the ***right balance*** between all the ***trade-offs*** during the [design process](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design.md#system-design-principles-and-processes)?
  - How do they know the right questions to ask?
  - How do they define clear objectives?
  - How do they define and measure success?
  - How do they choose the best Platform Design, Tools and Practices for your Workload?
  - How do they choose the best UX/UI/Frontend Design, Tools and Practices for your Workload?
  - How do they choose the best [Storage/Database/Data Design](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Theory-and-Concepts.md#the-concept-of-data-and-its-application-in-computer-science), Tools and Practices for your Workload?
  - How do they choose the best Network Design, Tools and Practices for your Workload?
  - How do they choose the best Compute Design, Tools and Practices for your Workload?
  - How do they choose the best Data Structures, Algorithms and Protocols for your Workload??
  - How do they choose the best Standards for your Workload?? Do you standardize on implementation or semantics?<br>
  - How do they choose the best Security Design, Tools and Policies/Practices for your Workload?
  - How do they choose the best Observability/Telemetry/Monitoring/Logging/Tracing/Analytics Design, Tools and Practices for your Workload?
  - How do they choose the best Testing/Benchmarking Design, Tools and Practices for your Workload?
  - How do they choose the best Programming Language and IDE to implement your Workload?
  - How do they choose the best SDLC, CI/CD, and Distributed Version Control System Tools and Practices/Workflows for your Workload?
+ How do your Architects/Designers/Programmers/Teams/Departments communicate and how often?
  - In person Meetings, Email, Mailing Lists, Chat, Slack, Discord, Mastadon, IRC; Video: Office365, MSTeams, Zoom, WebEx, GoToMeeting?
  - Every Week, Daily (15 min scrum), every Month, Never?
+ What Environment/Platform does your workload run?
  - [OnPrem, Cloud-Based, Cloud Native, Multi-Cloud, Hybrid Cloud; Private Cloud, Public Cloud](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Topics.md#it-industry-definitionsbuzzwords)?
  - Bare Metal, VMs, Containers, Mixture of All of them?
  - Cloud Agnostic/Cloud Native?
  - Self-Hosted/Fully Managed?
  - Open Source Software/Enterprise Software?
  - Monolithic, Microservices, Serverless?
  - Request-Response (Synchronous)/Event-driven (Asynchronous)?
  - Multitenant/Single Tenant?
  - What Cloud Provider(s) and Services do you use?
    - AWS has over [535 Cloud Services spanning 20+ Categories](https://www.antvaset.com/c/21gjdl7gz4) 
    - GCP has over [32 Cloud Services](https://cloud.google.com/products/) [spanning 7 Categories](https://www.infiflex.com/what-are-the-google-cloud-platform-services)
    - Azure has over [295 Cloud Services spanning 21 Categories](https://azure.microsoft.com/en-us/products/) 
+ What is your Disaster Recovery Plan (DRP)?
  - How often to you practice your DRP?
  - How do you [Failover](https://en.wikipedia.org/wiki/Failover) your workload?
  - What are your Incidence Response and Root Cause Analysis (RCA) procedures.
+ What is your Network Design?
  - Where are your [High-Level](https://en.wikipedia.org/wiki/High-level_design) Network Architecture/Design Diagrams?
  - Describes your Network: Traffic Ingress/Egress, Routers, Switches, Firewalls, Load Balancers, API Gateways, iPXE, Redfish, NTP/PPT, DNS, DHCP, BGP (eBGP,iBGP), OSPF; CDNs, Edge Networking; [Failover](https://en.wikipedia.org/wiki/Failover), Redundancy
  - What are the results of your Network capacity planning?
  - What Network Tools do you use?
    - RANCID, Netcat, Netbox, iperf
+ What is your [Storage/Database/Data Design](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Theory-and-Concepts.md#the-concept-of-data-and-its-application-in-computer-science)?
  - Where are your [High-Level](https://en.wikipedia.org/wiki/High-level_design) Storage/Data Architecture/Design Diagrams?
  - Data Lake, Wherehouse, Data Catalog
  - Relational, NoSQL, Document Oriented, Graph DB
  - Block Storage, Filesystem Storage, Object Storage
  - CePH, BigTable, DynamoDB
  - How do you [snapshot](https://en.wikipedia.org/wiki/Snapshot_(computer_storage))/[replicate](https://en.wikipedia.org/wiki/Replication_(computing))/[migrate](https://en.wikipedia.org/wiki/Data_migration)/[backup](https://en.wikipedia.org/wiki/Backup) large amounts of data?
  - What are the results of your Storage capacity planning?
  - What Data Tools do you use?
    - DataDog, Splunk, Greylog
+ What is your Compute Design?
  - Where are your [High-Level](https://en.wikipedia.org/wiki/High-level_design) Compute Architecture/Design Diagrams?
  - AWS EC2 VMs, OnPrem Servers/VMs/Containers
  - What are the results of your Compute capacity planning?
+ What Infrastructure Provisioning Tools do you use?
  - Terraform, Ansible, Nomad, Kubernetes?
+ What Programming Languages do you use?
  - Python, Go, Bash, Rust, C, C++, Java, Javascript
  - What Programming Tools and/or Frameworks do you use?
    - IDEs: VSC, Vim, Emacs
    - Distributed Version Control System: Git, Github, Gitlab
    -  Programming Style Guides
    -  Frameworks: Angular, Kafka, React, Backbone
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
+ Read my [Systems Design Topics](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Topics.md) information that adds more details to what we've already discussed here.
+ Read my [Systems Design Kubernetes](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Kubernetes.md) information for how I apply these principles to a Kubernetes Environment.
+ Read my [Systems Design AI](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-AI.md) information for how AI helps in System Design.
+ Read my [Systems Design OnPrem](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-OnPrem.md) information for how to setup an OnPrem Infrastructure.
+ Read my [Theory and Concepts that will make you a better Systems Designer](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Theory-and-Concepts.md) information for how theory helps in Systems Design.
