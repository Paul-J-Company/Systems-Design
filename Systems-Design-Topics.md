## System Design Topics:

### System Property Definitions:
Security:<br>
&ensp;&ensp;Security is a Full Stack endeavor.<br>
&ensp;&ensp;Security is a complete field of study on to itself.<br>
&ensp;&ensp;[Visualizing Cybersecurity](https://media.licdn.com/dms/image/C4E12AQEAjtq7T89h9A/article-cover_image-shrink_600_2000/0/1619282865626?e=1702512000&v=beta&t=yVJFR4c5VswXWv1qn-oWX6GYKfHYD8hgFgy1eSlEgU0)<br>
&ensp;&ensp;[Cybersecurity Domain Map ver 3.0](https://www.linkedin.com/pulse/cybersecurity-domain-map-ver-30-henry-jiang)<br>
&ensp;&ensp;[Cybersecurity Domain Map ver 3.1](https://media.licdn.com/dms/image/C4E12AQFEgFdbEtEl3Q/article-inline_image-shrink_1500_2232/0/1619282900607?e=1702512000&v=beta&t=y_bX1iXK-yLdgRHAgLp6UKHdl1IlqIna1RW0TN5LPF4)<br>
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
&ensp;&ensp;and also decreases Opex because there are fewer things to maintain.<br>
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
&ensp;&ensp;but decreases Opex because there are fewer things to maintain.<br>

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

Optimization:<br>
&ensp;&ensp;Optimization is a Full Stack endeavor.<br>
&ensp;&ensp;Optimization is finding the maxima of key performance metrics.<br>
&ensp;&ensp;Optimization is the selection of a best element, with regard to some criterion, from some set of available alternatives.<br>
&ensp;&ensp;A quote from Donald Knuth on Optimization:<br>
&ensp;&ensp;&ensp;&ensp;"We should forget about small efficiencies, say about 97% of the time: premature optimization is the root of all evil.<br>
&ensp;&ensp;&ensp;&ensp;&nbsp;Yet we should not pass up our opportunities in that critical 3%."<br>

High Availability (HA):<br>
&ensp;&ensp;High Availability is a Full Stack endeavor.<br>
&ensp;&ensp;High Availability is about adding redundancy which eliminates all [single points of failure](Single point of failure).<br>
&ensp;&ensp;HA increases resiliency because the system avoids failures by eliminating [single points of failure](Single point of failure).<br>
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
&ensp;&ensp;&ensp;&ensp;sitting there waiting to handle traffic, so when things [failover](https://en.wikipedia.org/wiki/Failover) there's a non-zero<br>
&ensp;&ensp;&ensp;&ensp;probability that the device will fail because you haven't been using it.<br>
&ensp;&ensp;&ensp;&ensp;Is the hot-standby configuration right? Is it having hardware issues?<br>
&ensp;&ensp;2) Active-Passive: aka., Hot Standby<br>
&ensp;&ensp;&ensp;&ensp;Each device should be configured to have the same capacity,<br>
&ensp;&ensp;&ensp;&ensp;so when a failure happens there is no loss of service.<br>
&ensp;&ensp;&ensp;&ensp;If you're going to configure each device at 100% capacity<br>
&ensp;&ensp;&ensp;&ensp;you might as well do an active-active configuration.<br>
&ensp;&ensp;&ensp;&ensp;In a active-passive scenario you must schedule regular [failovers](https://en.wikipedia.org/wiki/Failover)<br>
&ensp;&ensp;&ensp;&ensp;to verify the hot-standby device is working properly.<br>

### System Design Principles and Processes
1) Practice these Design Priciples:<br>
   Practice does NOT make Perfect!<br>
   Perfect Practice makes Perfect!<br>
   Practice!, Practice!, Practice!<br>
   **There's no substitute for doing!**<br>
   **Book learning will only get you so far.**<br>
2) Efficient Communication:<br>
   ABC = Accurate, Brief and Clear<br>
   CCC = Correct, Concise, Clear<br>
   Rule #1: Know your audience!<br>
   Always stay calm and rational.<br>
   You want a good signal-to-noise ration (SNR).<br>
   Signal is what you want.<br>
   Noise is what you don't want.<br>
   Always be kind!<br>
   Being a good person is more important than any technical skill you may have or aquire.<br>
3) Design is about making tradeoffs and compromises at all levels of your System.<br>
   e.g., Security vs. Convenience, Capex vs. Opex, etc.<br>
   Design is a Full Stack endeavor.<br>
   Identify all the trade-offs, bottlenecks and [single points of failure](Single point of failure).<br>
   Have a broad knowledge of alternative technologies.<br>
   Ask many counter questions:<br>
   &ensp;&ensp;How many daily users?<br>
   &ensp;&ensp;What are the edge cases?<br>
   Get feedback from your stakeholders - Are these tradeoffs acceptable?<br>
   Don't forget capacity planning.<br>
   Validate your design.<br>
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
6) [Problem Decomposition:](https://en.wikipedia.org/wiki/Decomposition_(computer_science))<br>
7) [Keep it Simple Stupid: (KISS)](https://en.wikipedia.org/wiki/KISS_principle)<br>
   Simple is the opposite of complex.<br>
   Complexity is the enemy of clarity!<br>
   Simple does not always imply easy!<br>
 8) [Separation of Concerns: (SoP)](https://en.wikipedia.org/wiki/Separation_of_concerns)<br>
   [Separation of Content and Presentation](https://en.wikipedia.org/wiki/Separation_of_content_and_presentation)<br>
 9) [Single Responsibility Principle: (SRP)](https://en.wikipedia.org/wiki/Single_responsibility_principle)<br>
10) [Principle of Least Privilege:](https://en.wikipedia.org/wiki/Principle_of_least_privilege) aka., (PoLP), Principle of Least Authority (PoLA)<br>
11) [Principle of Compositionality:](https://en.wikipedia.org/wiki/Principle_of_compositionality)<br>
12) Abstraction:<br>
    See: "[General Abstractions](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#general-abstractions)"<br>
    See: "[Computer Abstractions](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#computer-abstractions)"<br>

### IT Industry Definitions/Buzzwords:
Buzzwords are one thing about the IT Industry I don't care for.<br>
Buzzwords are typically ambiguous and violate the Efficient Communications rule.<br>
IT Systems are complicated enough without having to add to the confusion with buzzwords.<br>
But as a rational person, you have to deal with reality, and sadly, buzzwords are a reality of today's modern IT Industry.<br>
Here is my attempt to apply Efficient Communication (filter the signal from the noise) to IT buzzwords.<br>
**A quick comment on the buzzwords Platform Engineering, DevOps, and Site Reliability Engineer (SRE):<br>**
Don't sweat the details of these 3 buzzwords, they all really mean the same thing:<br>
you have an infrastructure, people using that infrastructure (Ops, Developers, etc.)<br>
and your job is to design, build and maintain the infrastructure and make the people using it happy.<br>
The definition of "happy" is created by analyzing your Company's needs and objectives.<br>
[Wikipedia](https://en.wikipedia.org/wiki/Buzzword) and [Google](https://www.google.com/search?q=IT+buzzwords) are good sources for looking up these buzzwords.<br>
What is Free and Opensource?<br>
&ensp;&ensp;[The Open Source Definition:](https://opensource.org/osd/)<br>
&ensp;&ensp;[The Free Software Definition:](https://www.gnu.org/philosophy/free-sw.en.html#fs-definition)<br>
What is a Data Center?<br>
&ensp;&ensp;A [Data Center](https://www.youtube.com/watch?v=qUmLnSEVVDw) is a physical building located around the world that houses your Platforms, Systems, Workloads.<br>
&ensp;&ensp;There are currently [four data center tiers](https://phoenixnap.com/blog/data-center-tiers-classification), [ranked by performance and uptime](https://www.impactmybiz.com/blog/data-center-tiers-explained/<).<br>
&ensp;&ensp;[Azure Global Infrastructure](https://azure.microsoft.com/en-us/explore/global-infrastructure) Microsoft Azure is comprised of 300+ physical datacenters.<br>
&ensp;&ensp;[Facebook's](https://www.youtube.com/watch?v=hkT0QKDmCiY) The largest Facebook data center houses more than 400,000 computer servers.<br>
&ensp;&ensp;[AWS Data Centers Today: 100+ Locations, 1.5 Million Servers, and More](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiPgJmE4vaBAxVaD0QIHTYPB-8QFnoECBMQAw&url=https%3A%2F%2Fwww.cloudzero.com%2Fblog%2Faws-data-center-locations&usg=AOvVaw00IBauiqtFxZ3jWJ3jOZFk&opi=89978449)<br>
&ensp;&ensp;AWS has over 100 data centers globally, covering 31 AWS Regions, 99 Availability Zones,<br>
&ensp;&ensp;over 400 edge locations/local zones, and 245 countries and territories.<br>
&ensp;&ensp;[AWS Cloud Infrastructure](https://www.youtube.com/watch?v=q6WlzHLxNKI)<br>
&ensp;&ensp;[Google Cloud’s Data Center Locations: Regions and Availability Zones](https://dgtlinfra.com/google-cloud-data-center-locations/) Google operates or is developing 35 data centers around the world.<br>
&ensp;&ensp;[Google Data Centers](https://www.google.com/about/datacenters/)<br>
&ensp;&ensp;[Google Cloud Infrastructure](https://cloud.google.com/infrastructure)<br>
&ensp;&ensp;[How does Google design its data centers?](https://www.youtube.com/watch?v=9IZ4qPAL-vA)<br>
&ensp;&ensp;"Normal" deployed power density ranges from 5-6kW per rack,<br>
&ensp;&ensp;anything above that could be considered high density, up to around 30kW per rack.<br>
&ensp;&ensp;Some data centers exceed this, even achieving ultrahigh density of up to 50-60kW per rack.<br>
&ensp;&ensp;When it comes to data centers, more power in a smaller footprint equals more efficiency.<br>
&ensp;&ensp;In 2023, US data centers are expected to consume 100 billion kilowatt-hours of energy (100 GWh), according to one energy-usage report.<br>
&ensp;&ensp;As if that wasn't bad enough, each kilowatt-hour of energy requires two gallons of water to cool it.<br>
&ensp;&ensp;So for 2023 alone, that equates to some 250,000 Olympic-size swimming pools of water.<br>
&ensp;&ensp;[2023 Global Data Center Trends](https://www.cbre.com/insights/reports/global-data-center-trends-2023): Northern Virginia remains the world's largest data center market with 2,132 MW of total inventory.<br>
What is Infrastructure as Code (IaC)?<br>
&ensp;&ensp;IaC is a DevOps practice of managing infrastructure in a declarative manner using code,<br>
&ensp;&ensp;rather than manually configuring it through a graphical user interface.<br>
&ensp;&ensp;Declarative: The process of declaring your desired result and the system "learns" how to achieve it.<br>
&ensp;&ensp;Imperative: The process of explaining every step to accomplish a desired result.<br>
What is Infrastructure as a Catalog (InCa)?<br>
&ensp;&ensp;[Navigating the Evolution: Infrastructure as Catalog](https://thenewstack.io/navigating-the-evolution-infrastructure-as-catalog/)<br>
&ensp;&ensp;InCa is a conceptual framework focusing on declaring infrastructure components with precision,<br>
&ensp;&ensp;while the implementation details are separated and managed independently.<br>
&ensp;&ensp;InCa takes all the good stuff from IaC and streamlines it, making things more transparent and a lot easier to manage.<br>
&ensp;&ensp;InCa aims to enhance transparency and understanding of architecture.<br>
&ensp;&ensp;InCa ensures that all changes are auditable, reversible and thoroughly documented in Git.<br>
What is Software Defined X (SD-X)?<br>
&ensp;&ensp;The term Software Defined is related to IaC in the sense that it has to do with using **code** to manage something verses using a **GUI/Dashboard**.<br>
&ensp;&ensp;The difference between IaC and SD-X is that IaC is a more general term and SD-X is usually limited to networking devices, but that's a convention.<br>
&ensp;&ensp;Some SD terms include: SD-WAN, SD-LAN, SD-WLAN, SD-Security, etc. uggggh!!!!<br>
What is "as a Service" (aaS)?<br>
&ensp;&ensp;[aaS](https://en.wikipedia.org/wiki/As_a_service) is a postfix, attached to any service you can think of that is accessed via the Internet typically using a REST API over http/https.<br>
&ensp;&ensp;The term XaaS can mean "anything as a service".<br>
&ensp;&ensp;[Some aaS terms include:](https://www.auvik.com/franklyit/blog/aas-as-a-service-list/) SaaS, PaaS, FaaS, CaaS, ..., rediculous! Did I mention I hate buzzwords!<br>
What is Platform as a Service (PaaS)?<br>
&ensp;&ensp;[Platform as a Service (PaaS)](https://en.wikipedia.org/wiki/Platform_as_a_service) is an abstraction over infrastructure that runs applications and hosts stacks.<br>
&ensp;&ensp;PaaS supports custom workflows to enable teams to function efficiently.<br>
&ensp;&ensp;PaaS enables the introduction of new ways to build, run, and deploy apps easily.<br>
&ensp;&ensp;PaaS allows underlying technology to be swapped out with no impact on teams.<br>
What is Platform Engineering?<br>
&ensp;&ensp;Platform Engineering ensures that there isn't an "us and them" mentality,<br>
&ensp;&ensp;which leads to a bad overall customer experience.<br>
&ensp;&ensp;Platform Engineering is all about accelerating software delivery efficiency and velocity.<br>
&ensp;&ensp;Platform Engineering gives developers the tools they want to use.<br>
What is Site Reliability Engineering (SRE)?<br>
&ensp;&ensp;[Site Reliability Engineering: A Comprehensive Guide](https://semaphoreci.com/blog/site-reliability-engineering)<br>
&ensp;&ensp;SRE is all about performance and application/system reliability.<br>
&ensp;&ensp;SRE is the practice of using software tools to automate IT infrastructure<br>
&ensp;&ensp;tasks such as system management and application monitoring.<br>
&ensp;&ensp;SRE teams use software as a tool to manage systems, solve problems, and automate operations tasks.<br>
&ensp;&ensp;SRE constitutes practices aiming to enhance the reliability and availability of software systems.<br>
&ensp;&ensp;Merging software engineering, systems engineering, and operations,<br>
&ensp;&ensp;SRE focuses on designing, building, and maintaining large-scale, fault-tolerant systems with high reliability.<br>
&ensp;&ensp;SRE teams collaborate with developers to ensure newly introduced features prioritize reliability.<br>
&ensp;&ensp;A fundamental SRE principle is maximizing automation in tasks like infrastructure management, code deployment, and system monitoring.<br>
&ensp;&ensp;SRE also diminishes the mean time to recovery (MTTR) post incidents, ensuring rapid problem resolution, thus minimizing business impact.<br>
&ensp;&ensp;SRE vs. DevOps:<br>
&ensp;&ensp;DevOps represents a cultural and organizational model stressing synergy between development<br>
&ensp;&ensp;and operations units, aiming to boost software delivery speed and quality.<br>
&ensp;&ensp;Conversely, SRE is a specialized DevOps offshoot centering on reliability.<br>
&ensp;&ensp;Even though SRE teams liaise with both development and operations,<br>
&ensp;&ensp;their chief objective remains system reliability, continuous uptime, and scalability.<br>
&ensp;&ensp;Among the primary roles of an SRE team is incident management.<br>
&ensp;&ensp;When such events arise, the SRE team quickly identifies the problem, ascertains its origin, and executes solutions.<br>
&ensp;&ensp;SRE Roles & Responsibilities:<br>
&ensp;&ensp;&ensp;&ensp;SRE teams are typically responsible for ensuring that systems are always up and running.<br>
&ensp;&ensp;&ensp;&ensp;1) Monitoring: SRE teams use monitoring tools to detect issues as soon as possible.<br>
&ensp;&ensp;&ensp;&ensp;2) Incident Response: SRE teams respond to incidents and work to resolve them quickly and effectively.<br>
&ensp;&ensp;&ensp;&ensp;3) Automation: SRE teams automate repetitive tasks to reduce the likelihood of human error.<br>
&ensp;&ensp;&ensp;&ensp;4) Performance Engineering: SRE teams work to ensure that systems are performing well, even in the face of high traffic volumes.<br>
&ensp;&ensp;&ensp;&ensp;5) Capacity Planning: SRE teams plan for future growth and ensure that systems can handle increased traffic volumes.<br>
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
&ensp;&ensp;[DevOps is terrible](https://medium.com/@mbianchidev/2023-devops-is-terrible-ec88162c86d7)<br>
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
&ensp;&ensp;[Using DORA Metrics to Measure DevOps Success](https://devops.com/using-dora-metrics-to-measure-devops-success/)<br>
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
&ensp;&ensp;how you structure your Git repo: repo-per-app, repo-per-team, monrepo<br>
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
&ensp;&ensp;Loosely Coupled means you can change things without affecting anything outside itself.<br>
&ensp;&ensp;Loose Coupling can be thought of as a principle to increase availability through fault tolerance.<br>
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
&ensp;&ensp;Cloud Observability, Grafana Labs, Jaeger, SigNoz, AppDynamics<br>
What is Root Cause Analysis (RCA)?<br>
&ensp;&ensp;[Root Cause Analysis (RCA)](https://en.wikipedia.org/wiki/Root_cause_analysis) is a method of problem solving used for identifying the root causes of faults or problems.<br>
&ensp;&ensp;[My Personal Incident RCA Report](https://github.com/Paul-J-Company/Systems-Design/blob/main/Systems-Design-Incident-Report-RCA.md) is a method of problem solving used for identifying the root causes of faults or problems.<br>
What is Incidence Management?<br>
Incident management often involves:<br>
&ensp;&ensp;1) Detection:<br>
&ensp;&ensp;&ensp;&ensp;Utilizing monitoring tools for prompt incident identification.<br>
&ensp;&ensp;2) Escalation:<br>
&ensp;&ensp;&ensp;&ensp;Should the initial team fail to resolve an issue,<br>
&ensp;&ensp;&ensp;&ensp;escalation to a senior member occurs.<br>
&ensp;&ensp;3) Diagnosis:<br>
&ensp;&ensp;&ensp;&ensp;Root cause determination of the incident.<br>
&ensp;&ensp;4) Mitigation:<br>
&ensp;&ensp;&ensp;&ensp;Steps are taken to lessen the incident's impact.<br>
&ensp;&ensp;5) Resolution:<br>
&ensp;&ensp;&ensp;&ensp;Final resolution and measures to avert future recurrences.<br>
What is [WebAssembly](https://en.wikipedia.org/wiki/WebAssembly)?<br>
&ensp;&ensp;[WebAssembly:](https://webassembly.org/)<br>
&ensp;&ensp;WebAssembly (abbreviated Wasm) is a binary instruction format for a stack-based virtual machine.<br>
&ensp;&ensp;Wasm is designed as a portable compilation target for programming languages,<br>
&ensp;&ensp;enabling deployment on the web for client and server applications.<br>
&ensp;&ensp;The main goal of WebAssembly is to enable high-performance applications on web pages,<br>
&ensp;&ensp;"but it does not make any Web-specific assumptions<br>
&ensp;&ensp;&ensp;or provide Web-specific features,<br>
&ensp;&ensp;&ensp;so it can be employed in other environments as well."<br>
What is eBPF?<br>
&ensp;&ensp;[eBPF](https://en.wikipedia.org/wiki/EBPF)<br>
&ensp;&ensp;[eBPF](https://ebpf.io/) stands for extended Berkeley Packet Filter (eBPF)<br>
&ensp;&ensp;eBPF is a technology that can run programs in a privileged context such as the operating system kernel.<br>
&ensp;&ensp;eBPF is used to safely and efficiently extend the capabilities of the kernel at runtime<br>
&ensp;&ensp;without requiring changes to kernel source code or loading kernel modules.<br>
What are Protocol Buffers?<br>
&ensp;&ensp;[Protocol Buffers:](https://protobuf.dev/)<br>
&ensp;&ensp;[Protocol Buffers](https://en.wikipedia.org/wiki/Protocol_Buffers) is a data format used to serialize structured data.<br>
&ensp;&ensp;Google use Protocol Bufferes to implement gRPC.<br>
&ensp;&ensp;Protocol Buffers are similar to the Apache Thrift, Ion, and Microsoft Bond protocols.<br>
What is gRPC?<br>
&ensp;&ensp;[gRPC](https://en.wikipedia.org/wiki/GRPC)<br>
&ensp;&ensp;gRPC is a modern, open source, high-performance remote<br>
&ensp;&ensp;procedure call (RPC) framework that can run anywhere.<br>
&ensp;&ensp;gRPC enables client and server applications to communicate transparently,<br>
&ensp;&ensp;and simplifies the building of connected systems.<br>
What is Single Pain of Glass?<br>
&ensp;&ensp;[Single pane of glass](https://www.mitel.com/features-benefits/single-pane-of-glass) is a term used throughout the IT and management fields relating to a management tool<br>
&ensp;&ensp;that unifies data or interfaces across several different sources and presents them in a single view.<br>

### The Six Pillars of Platform Engineering:
1) [Security:](https://thenewstack.io/the-6-pillars-of-platform-engineering-part-1-security/)<br>
2) [Pipeline (VCS, CI/CD):](https://thenewstack.io/the-6-pillars-of-platform-engineering-part-2-ci-cd-vcs-pipeline/)<br>
3) [Provisioning:](https://thenewstack.io/the-pillars-of-platform-engineering-part-3-provisioning/)<br>
4) [Connectivity:](https://thenewstack.io/the-pillars-of-platform-engineering-part-4-connectivity/)<br>
5) [Orchestration:](https://thenewstack.io/the-pillars-of-platform-engineering-part-5-orchestration/)<br>
6) [Observability:](https://thenewstack.io/the-pillars-of-platform-engineering-part-6-observability/)<br>

### Principles of GitOps:
1) Declarative:<br>
&ensp;&ensp;A system managed by GitOps must have it's state expressed declaratively.<br>
2) Versioned and Immutable:<br>
&ensp;&ensp;Desired state is stored in a way that enforces immutability,<br>
&ensp;&ensp;versioning and retains a complete version history.<br>
3) Pulled Automatically:<br>
&ensp;&ensp;Software agents automatically pull the desired state declarations from the source.<br>
4) Continuously Reconciled:<br>
&ensp;&ensp;Software agents continuously observe actual system state<br>
&ensp;&ensp;and attempt to apply the desired state.<br>

### Three Levels of Maturity for Infrastructure Automation:
1) Ad-hoc:<br>
   A mix of manual, scripted and niche infrastructure methods.<br>
   People-intensive and error-prone.<br>
2) Automated:<br>
   Enables infrastructure to be created, administrated and supported without needing<br>
   increasing numbers of experts who are in high demand and short supply.<br>
3) Frictionless:<br>
   Consistent, simple, measurable and secure infrastructure automation.<br>
   Removes all manual work, reduces complexity and fragmentation, ensuring<br>
   the infrastructure is governed, secure and accountable to the business.<br>
     
### Steps to Secure Your CI/CD Pipelines 
1) Security IN the Pipeline (SIP):<br>
   SIP involves ensuring developers are not shipping anything inherently insecure into production.<br>
   Therefore, whatever code flows through the CI/CD pipeline must be vetted to ensure it has no security flaws or misconfigurations.<br>
2) Security OF the Pipeline (SOP):<br>
   SOP has to do with the security of the software delivery chain itself.<br>
   SOP focuses on the security posture of the actual systems and tools that compromise the software delivery chain.<br>
3) Security Around the Pipeline (SAP):<br>
   SAP is necessary to ensure that attackers can't push code directly into production.<br>
   An example, no single developer can publish to production unless approved by two reviewers.<br>

### Advantages of Event-Driven Architectures (EDAs)
EDAs are a way of designing and building systems that are based on the exchange of events.<br>
Events are notifications of some change in state or data, and they are typically<br>
published by one component and consumed by another in real time.<br>
EDAs can:<br>
1) Decouple systems that can be independently scaled and updated.<br>
2) Handle high volumes of data with low latency.<br>
3) Support real-time processing and analytics.<br>
4) Be more scalable and resilient to failures.<br>

