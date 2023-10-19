## Theory and Concepts that will make you a better Systems Designer

### General Abstractions:
An [Abstraction](https://en.wikipedia.org/wiki/Abstraction) is hiding complexity and/or [hiding information](https://en.wikipedia.org/wiki/Information_hiding).<br>
[Abstraction in Computer Science](https://en.wikipedia.org/wiki/Abstraction_(computer_science)) is a simple interface that hides the complexity behind it.<br>
Another view on abstraction is the more abstract something is, the more general/implicit, and/or less specific/explicit/detailed it is.<br>
In a broader sense, Abstraction [simplifies](https://en.wikipedia.org/wiki/Simplicity) things.<br>
But remember, simple does not necessarily imply easy.<br>
An [Abstraction Layer](https://en.wikipedia.org/wiki/Abstraction_layer) includes the following concepts:<br>
&ensp;&ensp;[Interface:](https://en.wikipedia.org/wiki/Interface_(computing)) See: ABI, API, HAL; A good rule of thumb is if you see the word Interface, you're probably talking about an abstraction.<br>
&ensp;&ensp;[Encapsulation:](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)) See: [ACID](https://en.wikipedia.org/wiki/ACID)<br>
&ensp;&ensp;[Modularity:](https://en.wikipedia.org/wiki/Modularity)<br>
&ensp;&ensp;&ensp;&ensp;[Criteria for Modularization](https://www.win.tue.nl/~wstomv/edu/2ip30/references/criteria_for_modularization.pdf)<br>
&ensp;&ensp;&ensp;&ensp;[Modular Design](https://en.wikipedia.org/wiki/Modular_design)<br>
&ensp;&ensp;[Markov Blanket:](https://en.wikipedia.org/wiki/Markov_blanket)<br>
&ensp;&ensp;[Coupling:](https://en.wikipedia.org/wiki/Coupling_(computer_programming))<br>
&ensp;&ensp;&ensp;&ensp;[Loose Coupling](https://en.wikipedia.org/wiki/Loose_coupling) increases availability through fault tolerance<br>
&ensp;&ensp;[Cohesion:](https://en.wikipedia.org/wiki/Cohesion_(computer_science))<br>
&ensp;&ensp;&ensp;&ensp;[Cohesion Metrics](https://www.aivosto.com/project/help/pm-oo-cohesion.html)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;A cohesive class performs one function.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;A non-cohesive class performs two or more **unrelated** functions.<br>
&ensp;&ensp;[Unix Philosophy:](https://en.wikipedia.org/wiki/Unix_philosophy)<br>
&ensp;&ensp;[Continuous:](https://en.wikipedia.org/wiki/Continuity)<br>
&ensp;&ensp;[Discrete:](https://en.wikipedia.org/wiki/Discrete_mathematics)<br>
&ensp;&ensp;[Isolation:](https://en.wikipedia.org/wiki/Isolation_lemma)<br>
&ensp;&ensp;[Autonomy:](https://en.wikipedia.org/wiki/Learner_autonomy)<br>
&ensp;&ensp;[Autonomic](https://en.wikipedia.org/wiki/Autonomic_computing)<br>
&ensp;&ensp;[Independent:](https://en.wikipedia.org/wiki/Linear_independence)<br>
&ensp;&ensp;[Disjoint](https://en.wikipedia.org/wiki/Disjoint_union) [[1]](https://en.wikipedia.org/wiki/Disjoint_sets) [[2]](https://en.wikipedia.org/wiki/Disjoint-set_data_structure)<br>
&ensp;&ensp;[Mutual Exclusivity](https://en.wikipedia.org/wiki/Mutual_exclusivity)<br>

### Computer Abstractions:
Introduction:<br>
&ensp;&ensp;As mentioned above "[Your System is a Stack of Abstract Layers](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#your-system-is-a-stack-comprised-of-abstract-layers)".<br>
&ensp;&ensp;I use the terms Layers and Levels interchangably.<br>
&ensp;&ensp;In other words, Layers and Levels are synonyms/equivalent.<br>
&ensp;&ensp;Every layer has it's own [language](https://en.wikipedia.org/wiki/Category:Language)/[vocabulary](https://en.wikipedia.org/wiki/Category:Vocabulary)/[terminology](https://en.wikipedia.org/wiki/Category:Terminology)/[nomenclature](https://en.wikipedia.org/wiki/Nomenclature).<br>
&ensp;&ensp;Every layer produces and Emergent Higher Layer by defining an Interface.<br>
&ensp;&ensp;An Interface is the location where objects interact/couple.<br>
&ensp;&ensp;I call the combination of all the Layers of your System the "Full Stack".<br>
&ensp;&ensp;John Ousterhout, creator of the TCL Language likes to ask the following question:<br>
&ensp;&ensp;"What is the most important concept in Computer Science?"<br>
&ensp;&ensp;He asked Donald Knuth this question and his answer was: "Layers of Abstraction".<br>
&ensp;&ensp;John Ousterhout's answer to this question was: "[Problem Decomposition](https://www.youtube.com/watch?v=lgZ7Cxt5uIU#t=00h03m56s)".<br>

There are 3 Major Types of Computer Abstraction:<br>
1. One-to-Many Abstraction:<br>
   **Appears and behaves like one thing, but is actually many things.**<br>
   Network Abstractions:<br>
   &ensp;&ensp;[Load Balancer:](https://en.wikipedia.org/wiki/Load_balancing_(computing)) hardware-based and software-based<br>
   &ensp;&ensp;[API Gateway:](https://en.wikipedia.org/wiki/API_management#Gateway)<br>
   &ensp;&ensp;[1-to-Many NAT/PAT:](https://en.wikipedia.org/wiki/Network_address_translation#One-to-many_NAT)<br>
   &ensp;&ensp;[Forward Proxy:](https://en.wikipedia.org/wiki/Proxy_server#Forward_proxies)<br>
   &ensp;&ensp;[Reverse Proxy:](https://en.wikipedia.org/wiki/Reverse_proxy)<br>
   &ensp;&ensp;[HSRP](https://en.wikipedia.org/wiki/Hot_Standby_Router_Protocol)/[VRRP](https://en.wikipedia.org/wiki/Virtual_Router_Redundancy_Protocol)/[CARP:](https://en.wikipedia.org/wiki/Common_Address_Redundancy_Protocol)<br>
   &ensp;&ensp;[Link Aggregation Group (LAG)](https://en.wikipedia.org/wiki/Link_aggregation)/[Link Aggregation Control Protocol (LACP):](https://en.wikipedia.org/wiki/Link_aggregation#Link_Aggregation_Control_Protocol) aka., NIC Bonding/Teaming/Trunking/Bundling/Channeling<br>
   &ensp;&ensp;[Multi-Chassis Link Aggregation Group (MLAG):](https://en.wikipedia.org/wiki/Multi-chassis_link_aggregation_group)<br>
   Storeage Abstractions:<br>
   &ensp;&ensp;[RAID:](https://en.wikipedia.org/wiki/Raid)<br>
   &ensp;&ensp;[Controlled Replication Under Scalable Hashing (CRUSH):](https://ceph.com/assets/pdfs/weil-crush-sc06.pdf)<br>
   Compute Abstractions:<br>
   &ensp;&ensp;[Cluster:](https://en.wikipedia.org/wiki/Computer_cluster)<br>
   &ensp;&ensp;[Cloud Computing](https://en.wikipedia.org/wiki/Cloud_computing)<br>
2) Local-Remote Abstraction:<br>
   **Appears and behaves like a local resource, but is actually a remote resource.**<br>
   Storage Abstractions:<br>
   &ensp;&ensp;[Clusterd Filesystems:](https://en.wikipedia.org/wiki/Clustered_file_system) aka., Distributed Filesystems<br>
   &ensp;&ensp;[Network File System (NFS):](https://en.wikipedia.org/wiki/Network_File_System)<br>
   &ensp;&ensp;[Samba](https://en.wikipedia.org/wiki/Samba)/[SMB/CIFS](https://en.wikipedia.org/wiki/Server_Message_Block):<br>
   Compute Abstractions:<br>
   &ensp;&ensp;[Application Program Interface (API):](https://en.wikipedia.org/wiki/API)<br>
   &ensp;&ensp;[RPC](https://en.wikipedia.org/wiki/Remote_procedure_call)<br>
   &ensp;&ensp;[gRPC](https://en.wikipedia.org/wiki/GRPC)<br><br>
3) [Emulation](https://en.wikipedia.org/wiki/Emulator)/[Simulation](https://en.wikipedia.org/wiki/Computer_simulation)/[Virtualization](https://en.wikipedia.org/wiki/Virtualization) Abstraction:<br>
   **Appears and behaves like one thing, but is actually another.**<br>
   The Abstraction of [Information:](https://en.wikipedia.org/wiki/Information)<br>
   &ensp;&ensp;The term bit is short for "**b**inary dig**it**".<br>
   &ensp;&ensp;A [bit](https://en.wikipedia.org/wiki/Bit) is the lowest level of abstraction in Computer Science.<br>
   &ensp;&ensp;Without getting too techincal or philisophical,<br>
   &ensp;&ensp;a bit should only represent two states (thus the word binary, latin for "consisting of two") and persist over time.<br>
   &ensp;&ensp;The assignment of meaning to a collection of bits is the most powerful form of<br>
   &ensp;&ensp;abstraction because without it, information has no meaning and does not persist.<br>
   &ensp;&ensp;You can assign any meaning you want to a collection of bits, but we use [Boolean Algebra](https://en.wikipedia.org/wiki/Boolean_algebra) to assign meaning.<br>
   &ensp;&ensp;The reason for this is very philosophical and deep, and rooted in [Information Theory](https://en.wikipedia.org/wiki/Information_theory) and [Communication Theory](https://en.wikipedia.org/wiki/Communication_theory).<br>
   &ensp;&ensp;See: "[Theory and Concepts that will make you a better Systems Designer]()"<br>
   <br><br>
   &ensp;&ensp;If you're interested in deep diving, start by reading [Claude Shannon's](https://en.wikipedia.org/wiki/Claude_Shannon) seminal 1948 paper "[A Mathematical Theory of Communication](https://people.math.harvard.edu/~ctm/home/text/others/shannon/entropy/entropy.pdf)".<br>
   &ensp;&ensp;Follow that up with "[Computing Machinery and Intelligence](https://en.wikipedia.org/wiki/Computing_Machinery_and_Intelligence)" by [Alan Turning](https://en.wikipedia.org/wiki/Alan_Turing).<br>
   &ensp;&ensp;Follow that up with "[Church's Lambda Calculus](https://en.wikipedia.org/wiki/Lambda_calculus)/[The λ-Calculus and Type Theory](https://plato.stanford.edu/entries/church/supplementD.html)" and the "[Chruch Turing Thesis](https://en.wikipedia.org/wiki/Church%E2%80%93Turing_thesis)" by [Alonzo Church](https://en.wikipedia.org/wiki/Alonzo_Church)<br>
   &ensp;&ensp;Follow that up with "[Principia Mathematica](https://en.wikipedia.org/wiki/Principia_Mathematica)" by [Alfred North Whitehead](https://en.wikipedia.org/wiki/Alfred_Whitehead) and [Bertrand Russell](https://en.wikipedia.org/wiki/Bertrand_Russell).<br>
   &ensp;&ensp;Follow that up with "[Certain Factors Affecting Telegraph Speed](https://monoskop.org/images/9/9f/Nyquist_Harry_1924_Certain_Factors_Affecting_Telegraph_Speed.pdf)" and "[Certain Topics in Telegraph Transmission Theory](https://bayes.wustl.edu/Manual/CertainTopicsInTelegraphTransmissionTheory.pdf)" by [Harry Nyquist](https://en.wikipedia.org/wiki/Harry_Nyquist)<br>
   &ensp;&ensp;Follow that up with "[Transmission of Information](https://monoskop.org/images/a/a6/Hartley_Ralph_VL_1928_Transmission_of_Information.pdf)" by [Ralph Hartley](https://en.wikipedia.org/wiki/Ralph_Hartley)<br>
   &ensp;&ensp;Information Theory and Communication Theory is a rich field of study and worth the deep dive.<br>
   System Level Abstractions:<br>
   &ensp;&ensp;Bottom line: a computer system is nothing more than a series of abstractions layered on top of each other!<br>
   &ensp;&ensp;[Operating System (OS) Abstractions:](https://en.wikipedia.org/wiki/Operating_system)<br>
   &ensp;&ensp;[Virtual Reality (VR)](https://en.wikipedia.org/wiki/Virtual_reality)<br>
   &ensp;&ensp;[Augmented Reality (AR)](https://en.wikipedia.org/wiki/Augmented_reality)<br>
   &ensp;&ensp;[Mixed Reality (MR)](https://en.wikipedia.org/wiki/Mixed_reality)<br>
   Network Abstractions:<br>
   &ensp;&ensp;OS Abstraction Implements:<br>
   &ensp;&ensp;[Virtual Routing and Forwarding: (VRF)](https://en.wikipedia.org/wiki/Virtual_routing_and_forwarding)<br>
   &ensp;&ensp;[Virtual LAN (VLAN):](https://en.wikipedia.org/wiki/VLAN)<br>
   &ensp;&ensp;[Virtual Private Network (VPN):](https://en.wikipedia.org/wiki/Virtual_private_network) aka., Tunnel<br>
   &ensp;&ensp;[Overlay Network:](https://en.wikipedia.org/wiki/Overlay_network)<br>
   &ensp;&ensp;[TCP/IP Stack:](https://en.wikipedia.org/wiki/Internet_protocol_suite)<br>
   &ensp;&ensp;[OSI Model:](https://en.wikipedia.org/wiki/OSI_model)<br>
   Storage Abstractions:<br>
   &ensp;&ensp;OS Abstraction Implements:<br>
   &ensp;&ensp;[Virtual Memory:](https://en.wikipedia.org/wiki/Virtual_memory)<br>
   &ensp;&ensp;[Filesystem:](https://en.wikipedia.org/wiki/File_system)<br>
   &ensp;&ensp;[Cache:](https://en.wikipedia.org/wiki/Cache_(computing))<br>
   &ensp;&ensp;[CNI](https://github.com/containernetworking/cni)<br>
   &ensp;&ensp;[CSI](https://github.com/container-storage-interface/)<br>
   Compute Abstractions:<br>
   &ensp;&ensp;OS Abstraction Implements:<br>
   &ensp;&ensp;[Virtual Machines (VMs):](https://en.wikipedia.org/wiki/Virtual_machine)<br>
   &ensp;&ensp;&ensp;&ensp;[Type-1 Hypervisor:](https://en.wikipedia.org/wiki/Hypervisor#Classification) aka , VMM<br>
   &ensp;&ensp;&ensp;&ensp;[Type-2 Hypervisor:](https://en.wikipedia.org/wiki/Hypervisor#Classification)<br>
   &ensp;&ensp;&ensp;&ensp;[GuestOS:](https://www.techtarget.com/searchitoperations/definition/guest-OS-guest-operating-system) runs inside Type-1,2 Hypervisors<br>
   &ensp;&ensp;[Containers:](https://en.wikipedia.org/wiki/Containerization_(computing))<br>
   &ensp;&ensp;[List of Command Line Interpreters](https://en.wikipedia.org/wiki/List_of_command-line_interpreters), [Shell](https://en.wikipedia.org/wiki/Shell_(computing)), [Unix Shell](https://en.wikipedia.org/wiki/Unix_shell), [Terminal Emulator](https://en.wikipedia.org/wiki/Terminal_emulator) aka., Console. Terminal<br>
   &ensp;&ensp;[Application:](https://en.wikipedia.org/wiki/Application_software) aka., [Computer Program](https://en.wikipedia.org/wiki/Computer_program)<br>
   &ensp;&ensp;[Procedure/Subroutine/Function:](https://en.wikipedia.org/wiki/Function_(computer_programming))<br>
   &ensp;&ensp;[Job](https://en.wikipedia.org/wiki/Job_(computing))/[Unix Job](https://en.wikipedia.org/wiki/Job_control_(Unix))/[Batch Job](https://en.wikipedia.org/wiki/Batch_processing)<br>
   &ensp;&ensp;[Task:](https://en.wikipedia.org/wiki/Task_(computing))<br>
   &ensp;&ensp;[Process:](https://en.wikipedia.org/wiki/Process_(computing))<br>
   &ensp;&ensp;[Thread:](https://en.wikipedia.org/wiki/Thread_(computing))<br>
   &ensp;&ensp;[Fiber:](https://en.wikipedia.org/wiki/Fiber_(computer_science))<br>
   &ensp;&ensp;[Context Switching:](https://en.wikipedia.org/wiki/Context_switch)<br>
   &ensp;&ensp;[Driver:](https://en.wikipedia.org/wiki/Driver_(software)), [Device Driver](https://en.wikipedia.org/wiki/Device_driver)<br>
   &ensp;&ensp;Hardware Implements:<br>
   &ensp;&ensp;[Computer/Processor Instruction:](https://en.wikipedia.org/wiki/Instruction) one operation of a processor within a computer architecture<br>
   &ensp;&ensp;[Instruction Set Architecture (ISA):](https://en.wikipedia.org/wiki/Category:Instruction_set_architectures)<br>
   &ensp;&ensp;[Data](https://en.wikipedia.org/wiki/Data)<br>
   &ensp;&ensp;[Hardware Registers:](https://en.wikipedia.org/wiki/Hardware_register), [Processor Register](https://en.wikipedia.org/wiki/Processor_register)<br>
   &ensp;&ensp;[L1/L2/L3 Cache:](https://en.wikipedia.org/wiki/Cache_hierarchy)<br>
   &ensp;&ensp;[Pipelining:](https://en.wikipedia.org/wiki/Pipeline_(computing))<br>
   &ensp;&ensp;[Application Binary Interface (ABI):](https://en.wikipedia.org/wiki/Application_binary_interface)<br>
   &ensp;&ensp;[Hardware Abstraction Layer (HAL):](https://en.wikipedia.org/wiki/Hardware_abstraction#In_operating_systems)<br>

### The Concept of Data and its Application in Computer Science:
This section covers the concept of data and it's application in our main focus of<br>
System Design, Platform Engineering, SRE, and DevOps.<br>
What is [Data](https://en.wikipedia.org/wiki/Data)?<br>
&ensp;&ensp;Data is anything you can assign meaning to.<br>
&ensp;&ensp;Data in the context of digital computing is just a collection of bits.<br>
&ensp;&ensp;Technically, "data" is a plural noun (it is the plural form of the noun "datum").<br>
&ensp;&ensp;However, it is used with both singular and plural verbs.<br>
&ensp;&ensp;The term data (like bit) is so general, it almost has no meaning.<br>
&ensp;&ensp;Yet, it's probably the most important and most used word in all of modern Computer Science.<br>
What Is Structured Data?<br>
&ensp;&ensp;Structured data follows a specific format, making it easy to store and analyze.<br>
&ensp;&ensp;Examples of structured data include: customer information, transaction records and inventory lists.<br>
What Is Unstructured Data?<br>
&ensp;&ensp;Unstructured data refers to data that does not have a specific format or structure.<br>
&ensp;&ensp;This data type is often created by humans in forms such as text, images, videos, emails and social media posts.<br>
&ensp;&ensp;However, unstructured data can also include less common examples like protein structures,<br>
&ensp;&ensp;executable file hashes and human-readable code, among others - the possibilities are endless.<br>
&ensp;&ensp;Working with unstructured data can be challenging due to its lack of a standardized format.<br>
&ensp;&ensp;In addition, things become more complicated when it comes to querying and analyzing data,<br>
&ensp;&ensp;especially when compared to structured and semi-structured data.<br>
&ensp;&ensp;Unstructured data contains a wealth of information that can provide valuable insights into customer behaviors,<br>
&ensp;&ensp;market trends and other essential business metrics for more accurate decision-making.<br>
&ensp;&ensp;An astonishing 80% of newly generated data is unstructured.<br>
&ensp;&ensp;Examples of Unstructured Data include:<br>
&ensp;&ensp;&ensp;&ensp;Sensor data, Machine log data, Internet of Things (IoT) data, Computer vision data,<br>
&ensp;&ensp;&ensp;&ensp;Natural Language Processing (NLP) data, Web and application data, Emails, Text messages,<br>
&ensp;&ensp;&ensp;&ensp;Social media posts, Audio recordings, Handwritten notes, Meeting notes, Transcripts, User-generated content<br>
What is Semi-Structured Data? aka., Partially Structured Data<br>
&ensp;&ensp;Semi-structured data is a mixture of structured and unstructured data.<br>
&ensp;&ensp;Semi-structured data contains some level of organization, such as metadata or tags, but is not fully structured.<br>
&ensp;&ensp;Semi-structured data is commonly found in XML files, JSON documents and other data types that follow a specific schema.<br>
&ensp;&ensp;This type of data is usually stored in a NoSQL database like a wide-column store<br>
&ensp;&ensp;or object/document database since it cannot be directly stored in a relational database.<br>
What is High-Cardinality Data (HCD)?<br>
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
What is High-Dimensionality Data (HDD)?<br>
&ensp;&ensp;While high cardinality refers to a large number of data points (values) in a given attribute,<br>
&ensp;&ensp;dimensionality takes it further: how many attributes does an event have?<br>
&ensp;&ensp;Being able to analyze trends across many dimensions quickly is important<br>
&ensp;&ensp;when you're trying to figure out what changed but don't know what to ask.<br>
&ensp;&ensp;When you're trying to solve unknown-unknowns, high-dimensionality data is your friend.<br>
What is Curse of Dimensionality?<br>
&ensp;&ensp;The curse of dimensionality refers to various phenomena that arise when<br>
&ensp;&ensp;analyzing and organizing data in high-dimensional spaces that do not<br>
&ensp;&ensp;occur in low-dimensional settings such as the three-dimensional physical<br>
&ensp;&ensp;space of everyday experience.<br>
&ensp;&ensp;The amount of data needed often grows exponentially with the dimensionality.<br>
&ensp;&ensp;In high dimensional data, all objects appear to be sparse and dissimilar in many ways,<br>
&ensp;&ensp;which prevents common data organization strategies from being efficient.<br>
What are the 3 Main Storage Types?<br>
&ensp;&ensp;1) [Block Storage](https://en.wikipedia.org/wiki/Block_(data_storage))<br>
&ensp;&ensp;2) [Filesystem Storage](https://en.wikipedia.org/wiki/File_system), [List of File Systems](https://en.wikipedia.org/wiki/List_of_file_systems)<br>
&ensp;&ensp;3) [Object Storage](https://en.wikipedia.org/wiki/Object_storage)<br>
What is a [Database](https://en.wikipedia.org/wiki/Category:Databases)?<br>
&ensp;&ensp;A [Database](https://en.wikipedia.org/wiki/Database) is an organized collection of data (also known as a data store)<br>
&ensp;&ensp;stored and accessed electronically through the use of a [Database Management System (DBMS)](https://en.wikipedia.org/wiki/Database#Database_management_system).<br>
What is a Polystore?<br>
&ensp;&ensp;A polystore is the combining of different database technologies tailored for specific use cases,<br>
&ensp;&ensp;enabling organizations to optimize performance, scalability, and analytical capabilities throughout their infrastructure.<br>
&ensp;&ensp;Polystores embrace a hybrid approach, leveraging the strengths of different database technologies tailored to specific use cases.<br>
Database Models/Types:<br>
&ensp;&ensp;[Database Models](https://en.wikipedia.org/wiki/Category:Database_models)<br>
&ensp;&ensp;[Types of Databases](https://en.wikipedia.org/wiki/Category:Types_of_databases)<br>
&ensp;&ensp;[Database Software Comarisons](https://en.wikipedia.org/wiki/Category:Database_software_comparisons)<br>
  1) Relational Databases:<br>
     Examples: MySQL, Postgres<br>
     Best used for: most apps<br> 
     Not ideal for: Unstructured Data<br>
     Relational Database Transactions support [ACID](https://en.wikipedia.org/wiki/ACID) properties.<br>
     [A Relational Model of Data for Large Shared Data Banks by E.F. Codd](https://www.seas.upenn.edu/~zives/03f/cis550/codd.pdf)<br>
     [Database Normalization](https://en.wikipedia.org/wiki/Database_normalization)<br>
     [List of Relational Database Management Systems](https://en.wikipedia.org/wiki/List_of_relational_database_management_systems)<br>
     [Comparison of Relational Database Management Systems](https://en.wikipedia.org/wiki/Comparison_of_relational_database_management_systems)<br>
     [Database Shard](https://en.wikipedia.org/wiki/Shard_(database_architecture))<br>
     [Shared-Nothing Architecture](https://en.wikipedia.org/wiki/Shared-nothing_architecture)<br>
  2) NoSQL Databases:<br>
     Examples:<br>
     Best used for:<br> 
     [NoSQL](https://en.wikipedia.org/wiki/Category:NoSQL)<br>
     Schemaless Documents:<br>
       The number of fields, content and size of the document<br>
       can differ from one document to another in the same collection.<br>
  3) Key-Value Stores:<br>
     Examples: Redis, Memcached, etcd<br>
     Best used for:<br>
     [Key-value Databases](https://en.wikipedia.org/wiki/Category:Key-value_databases)<br>
       See: "Simularities between Object stores and key-value stores:"<br>
       See: "Differences between key-value stores and object stores:"<br>
  4) Document-Oriented Databases:<br>
     Examples: MongoDB, Google Firestore, DynamoDB, CouchDB<br>
     Best used for: Most apps, Games, IoT<br>
     Schema-less, No Normalization, Relational-ish Queries without Joins<br>
     Not good when you have disconnected but related data that is updated often like Social Media apps.<br>
     Not ideal for graphs.<br>
     [Document-Oriented Database](https://en.wikipedia.org/wiki/Document-oriented_database)<br>
       One of the main categories of NoSQL databases.<br>
       Document-oriented databases are inherently a subclass of the key-value store.<br>
     [How to Choose the Right Document-Oriented NoSQL Database for Your Application](https://dev.to/kalashin1/how-to-choose-the-right-document-oriented-nosql-database-for-your-application-3hac)<br>
     [Google Cloud Firestore vs MongoDB: Which Tool is Better for Your Next Project?](https://www.projectpro.io/compare/google-cloud-firestore-vs-mongodb)<br>
  5) Wide Column Store:<br>
     Examples:<br>
     Best used for:<br>
     [Wide Column Store](https://en.wikipedia.org/wiki/Wide-column_store)<br>
       A special type of NoSQL database.<br>
  6) Graph Database:<br>
     Examples: [neo4j](https://neo4j.com/blog/why-graph-databases-are-the-future), [Dgraph](https://dgraph.io/)<br>
     Best used for: Graphs, Knowledge Graphs, Recommendation Engines<br> 
     [Graph Databases](https://en.wikipedia.org/wiki/Category:Graph_databases)<br>
  7) Database Search Engine:<br>
     Examples: Apache Lucene, Solr, Meilisearch, Toshi, Quickwit, AWS Elasticsearch, Algolia, Sphinx, MS Azure Cognitive Search, Arango, Virtuoso, OpenSearch<br>
     Best used for: Search Engines, Typeahead<br>
     [Database Search Engine](https://en.wikipedia.org/wiki/Database_search_engine)<br>
     [Search-Engine Database](https://aws.amazon.com/nosql/search/)<br>
  8) In-Memory Databases:<br>
     Examples: Redis, <br>
     Best used for:<br>
     [In-Memory Database](https://en.wikipedia.org/wiki/In-memory_database)<br>
     [List of In-Memory Databases](https://en.wikipedia.org/wiki/List_of_in-memory_databases)<br>
  9) NewSQL Databases:<br>
     Examples:<br>
     Best used for:<br>
     [NewSQL](https://en.wikipedia.org/wiki/Category:NewSQL)<br>
 10) Time Series Databases:<br>
     Examples: Amazon Timestream,<br>
     Best used for: Time series data<br>
     [Time Series Database](https://en.wikipedia.org/wiki/Time_series_database)<br>
 11) Data Warehouses:<br>
     Examples: Apache Kudu, Amazon Redshift, Snowflake, HP Vertica, RDBMS<br>
     Best used for: read below for descriptions<br>
     [A data vault, warehouse, lake, and hub explained](https://www.cloverdx.com/blog/a-data-vault-warehouse-lake-and-hub-explained)<br>
     [10 Amazing Tools for Data Extraction in October 2023](https://www.analyticsinsight.net/10-amazing-tools-for-data-extraction-in-october-2023/)<br>
     &ensp;&ensp;Data extraction is the process of converting data from its source into a structured format for enhanced analysis and usability.<br>
     &ensp;&ensp;This structured format may involve organizing data into columns and rows, making it suitable for import into database management<br>
     &ensp;&ensp;or other programs; or organizing data to be consumed by Machine Learning Artificial Neural Networks; or any other format.<br>
     &ensp;&ensp;[Extract, Transform, Load (ETL)](https://en.wikipedia.org/wiki/Extract,_transform,_load)<br>
     [Data Warehousing](https://en.wikipedia.org/wiki/Category:Data_warehousing)<br>
     [Data Warehouse](https://en.wikipedia.org/wiki/Data_warehouse)<br>
     &ensp;&ensp;A data warehouse is a large structure that gathers data from multiple sources into one single repository.<br>
     &ensp;&ensp;A data warehouse is a consolidated, structured repository for storing data assets.<br>
     &ensp;&ensp;Data warehouses will store data in one of two ways: Star Schema or 3NF,<br>
     &ensp;&ensp;but these are only fundamental principles in how you store your data model.<br>
     &ensp;&ensp;Consolidate data and answer a business-related question.<br>
     &ensp;&ensp;How many users are visiting my product pages from North America?<br>
     &ensp;&ensp;[Visualizing a Datawarehouse with ETL](https://www.cloverdx.com/hs-fs/hubfs/Blog_Files/DWH/data-lake--fig1.png?width=2175&name=data-lake--fig1.png)<br>
     &ensp;&ensp;[Visualizing a Datawarehouse](https://www.cloverdx.com/hs-fs/hubfs/Blog_Files/DWH/data-lake--fig2.png?width=2175&name=data-lake--fig2.png)<br>
     [Data Mart](https://en.wikipedia.org/wiki/Data_mart)<br>
     [What is a data mart?](https://www.cloverdx.com/blog/what-is-a-data-mart)<br>
     &ensp;&ensp;A data mart is a smaller, specified data warehouse that focuses on one function or line of business.<br>
     &ensp;&ensp;This makes it much easier for departments to find the data that’s important to them.<br>
     &ensp;&ensp;These data marts are only accessible to groups within those business functions.<br>
     &ensp;&ensp;For example, a marketing manager can access a marketing-specific data mart,<br>
     &ensp;&ensp;but they wouldn't be able to view its financial counterpart.<br>
     [Data Vault](https://en.wikipedia.org/wiki/Data_vault)<br>
     &ensp;&ensp;A data vault is a system made up of a model, methodology and architecture<br>
     &ensp;&ensp;that is specifically designed to solve a complete business problem as requirements change.<br>
     &ensp;&ensp;A dynamic solution that gives business users access to all data (current and historical).<br>
     &ensp;&ensp;Used to give an audit trail and other scenarios where you need current and historical data.<br>
     &ensp;&ensp;[Visualizing a Data Vault](https://www.cloverdx.com/hs-fs/hubfs/Blog_Files/DWH/data-lake--fig5.png?width=2175&name=data-lake--fig5.png)<br>
     [Data Lake](https://en.wikipedia.org/wiki/Data_lake)<br>
     &ensp;&ensp;A data lake is a term that represents a methodology<br>
     &ensp;&ensp;of storing raw data in a single repository.<br>
     &ensp;&ensp;The type of data that's stored in the lake does not matter<br>
     &ensp;&ensp;and could be unstructured, structured, semi-structured, or binary.<br> 
     &ensp;&ensp;The fundamental idea for a data lake is to make available any/all data<br>
     &ensp;&ensp;from applications so your data team can provide insights on a business<br>
     &ensp;&ensp;problem or value proposition.<br>
     &ensp;&ensp;How do you know what data you need and what data you don't need?<br>
     &ensp;&ensp;How do you determine where the data resides in the lake?<br>
     &ensp;&ensp;Data lakes are typically used for:<br>
     &ensp;&ensp;reporting, visualization, analytics, and machine learning.<br>
     &ensp;&ensp;[Visualizing a Data Lake](https://www.cloverdx.com/hs-fs/hubfs/Blog_Files/DWH/data-lake--fig3.png?width=2175&name=data-lake--fig3.png)<br>
     [Data Hub](https://en.wikipedia.org/wiki/Data_hub)<br>
     &ensp;&ensp;A data hub is a centralized system where data is stored, defined, and served from.<br>
     &ensp;&ensp;We like to think of it as a hybrid of a data lake and a database warehouse,<br>
     &ensp;&ensp;as it provides a central repository for your applications to dump data.<br>
     &ensp;&ensp;A Data Hub also adds a level of harmonization at ingest<br>
     &ensp;&ensp;so the data is indexed and can easily be queried.<br> 
     &ensp;&ensp;Please note that this is not the same as a data warehouse architecture,<br>
     &ensp;&ensp;as the ETL processing is merely for indexing the data you have<br>
     &ensp;&ensp;rather than mapping it into a strict structure.<br>
     &ensp;&ensp;The challenge comes when you have to implement the data hub<br>
     &ensp;&ensp;and how can you harmonize all of your siloed data sources.<br>
     &ensp;&ensp;In general, we see the same use cases for a data hub as we would for a data lake:<br>
     &ensp;&ensp;[Visualizing a Data Hub](https://www.cloverdx.com/hs-fs/hubfs/Blog_Files/DWH/data-lake--fig4.png?width=2175&name=data-lake--fig4.png)<br>
     [Data Store](https://en.wikipedia.org/wiki/Data_store)<br>
     [What is an Operational Data Store (ODS)](https://www.cloverdx.com/blog/what-is-an-operational-data-store)<br>
     &ensp;&ensp;An operational data store (ODS) houses and processes transactional data in real-time.<br>
     &ensp;&ensp;ODSes collate current data from various source systems to provide a snapshot of your business at one point in time.<br>
     &ensp;&ensp;You can use the data inside for day-to-day data processing tasks, such as reporting and analysis.<br>
 12) Blockchain:<br>
     Examples:<br>
     Best used for:<br>
     [Blockchain-based Databases](https://en.wikipedia.org/wiki/Blockchain-based_database)<br>
     [Distributed Ledger](https://en.wikipedia.org/wiki/Distributed_ledger)<br>
 13) Distributed Filesystems: aka., Network File Systems<br>
     Examples: S3, CephFS, Lustre, NFS, etc.<br>
     Best used for:<br>
     [Distributed File Systems](https://en.wikipedia.org/wiki/Category:Distributed_file_systems)<br>
     [List of File Distributed Files Systems](https://en.wikipedia.org/wiki/List_of_file_systems#Distributed_file_systems)<br>
     [Clustered File Systems](https://en.wikipedia.org/wiki/Clustered_file_system#Distributed_file_systems)<br>
       The difference between a distributed file system and a distributed data store<br>
       is that a distributed file system allows files to be accessed using the<br>
       same interfaces and semantics as local files.<br>
       Distributed data stores, by contrast, require using a different API<br>
       or library and have different semantics (most often those of a database).<br>
 14) Distributed Data Store:<br>
     Examples: CockroachDB, Amazon Neptune, Apache Cassandra, Apache HBase, Apache Kudu, Bigtable, ClickHouse<br>
     Best used for:<br>
     [Distributed Data Storage](https://en.wikipedia.org/wiki/Category:Distributed_data_storage)<br>
     [Distributed Data Stores](https://en.wikipedia.org/wiki/Category:Distributed_data_stores)<br>
     [Distributed Data Store](https://en.wikipedia.org/wiki/Distributed_data_store)<br>
 15) Distribute Databases:<br>
     Examples:<br>
     Best used for:<br>
     [Distributed Database](https://en.wikipedia.org/wiki/Distributed_database)<br>
 16) Distributed Cache:<br>
     Examples:<br>
     Best used for:<br>
     [Distributed Cache](https://en.wikipedia.org/wiki/Distributed_cache)<br>
     [Distributed hash Table](https://en.wikipedia.org/wiki/Distributed_hash_table)<br>
 17) Cloud Databases:<br>
     Examples:<br>
     Best used for:<br>
     [Cloud Storage](https://en.wikipedia.org/wiki/Category:Cloud_storage)<br>
     [Cloud Database](https://en.wikipedia.org/wiki/Category:Cloud_databases)<br>
 18) Vector Databases:<br>
     Examples:<br>
     Best used for: Machine Learning<br>
     [Vector Database](https://en.wikipedia.org/wiki/Vector_database)<br>
 98) Polystore: aka., Polymorphic Databases, Multi-Model Database
     Examples: TypeDB, FaunaDB, BigDAWG<br> 
     Best used for: everything<br>
     Polystores are ACID compliant.<br>
     Polymorphic data means that in one collection you have many versions of document schema<br>
     (e.g. different field type, fields that occur in some documents etc.).<br>
     [Polystores: The Data Management Game Changer](https://thenewstack.io/polystores-the-data-management-game-changer/)<br>
     [The Case for Polystores](https://wp.sigmod.org/?p=1629)<br>
     [Polystore]()<br>
 99) [7 Database Paradigms](https://www.youtube.com/watch?v=W2Z7fbCLSTw)<br>

