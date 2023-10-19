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
