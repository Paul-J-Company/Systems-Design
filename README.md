# Systems-Design
Systems Design

System Properties:
You.want your System to be:
*) Secure: authentication, authorization, accounting (aaa)
*) Reliable: slow to fail
*) Robust:  quick to recover from failure.
*) Highly Available: 99.999
*) Performant: speed/latency
*) Scalable: capacity/bandwidth
*) Maintainable: automation
*) Cost Effective:  minimize Capex & Opex

Every business has business goals.
These System Properties align with the typical high level business goal of "satisfy your customers".

Your System is a Stack comprised of Layers:
*) Data Layer:
*) Network Layer:
*) Compute Layer:
*) Personnel Layer: all the departments and teams that are your business.

In order to achieve the above System Prooerties you have to apply the "best" practices, and the "best" technologies for each property,, at each layer of your stack.

This is a daunting task because there are so many options available and so many different ways your system will behave  depending on the choices you make at each lsyer. The permutations of choices and behavior quickly explode combinatorally.

This is what makes your System "complex"; and why it requires "experts" in System Design to achieve your goals.

So where do you begin?
It always starts with understanding your workload.
You can¿t make the "best choices" without understanding your workload intimately. 

Starting from a blank slate is different than inheriting an existing system infrastructure.

Here are some System Design questions to get you started:

System Design Questions:
Monitoring, Logging, Security to Questions.

*) How do you make decisions regarding all of the questions below?
Who are your Architects/Designers?
How do you find the right balance between all the trade-offs during the design process?
The only way to find the right balance between trade-offs is to consider the widest range of options available.
How do you choose the right DB to use?
How do you choose the right Data design?
How do you choose the best Cloud provider?
*) How do your Teams/Departments communicate:
   email, Slack, MSTeams, WebEx, GoToMeeting,?
*) What Security Policies do you have?
   What Security Tools do you use?
*) How do you Monitor your System?
   What Monitoring Tools do you use?
   Cloudwatch, CloudTrail, 
*) How do you Process your Logs?
   What Logging Tools do you use?
   Splunk, etc.
*) OnPrem, Cloud, MultiCloud or Hybrid?
   What Cloud Platform(s) and Services do you use?
   Where are your high-level Architecture Diagrams?
*) Bare Metal, VMs or Containers?
*) Monolithic, Microservices, Serverless?
*) Synchronous or Asynchronous Event-based?
*) Multitenant or Single Tenant?
*) What Programming Languages do you use?
*) What programming tools do you use? IDEs, Git, Style SmGuides, etc.
*) What is your SDLC, CI/CD, Deployment strategy (canary, green, etc.)

*) What Infrastructure tools do you use? iPXE, Terraform, Ansible, Kubernetes, Nomad etc.? NTP/PPT, DNS, DHCP, etc.
*) What, When, How and Why do you Test? What apps do you use for testing?
*) What is your Network Design? Where is your Network Architecture Diagrams? Connections in and out; BGP (eBGP,iBGP), OSPF, etc. CDN, Edge Networking, etc. Failover, Redundancy, etc.
*) What network tools do you use?
*) What is your Data Design?
Data Lake, Wherehouse, Relational, NoSQL, Document Oriented, Graph DB, etc. Object Storeage, Filesystem, Block, etc. CePH, etc. Snapshots, Replication, Backups, Data Migration, etc.
*) What data tools do you use? Datadog, etc.?

