## Systems Design OnPrem
I recommend viewing the corresponding [YouTube Playlist]() for this page.<br>
You can also jump down to the end of this page to review the [Additional Resources](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design-OnPrem.md#additional-resources) section.<br>

### On Prem Information
Introduction:<br>
&ensp;&ensp;The purpose of this section is to give a "bigpicture" view of an OnPrem Infrastructure.<br>
&ensp;&ensp;**I you're going Cloud Native/Fully Managed, you don't need to know a lot of the following steps.**<br>
&ensp;&ensp;The following is a description of a basic setup of an OnPrem Infrastructure:<br>
&ensp;&ensp;This is a quick, short, and incomplete list of necessities.<br>
&ensp;&ensp;I'm skipping Data Center topics like Generators, UPSes, Power Design, HVAC Cooling Design, Security,<br>
&ensp;&ensp;Peering Relationships and Negotiations, Cost Estimation, etc. because that really requires another full document to explain.<br>
&ensp;&ensp;And, I'm not a Data Center Design Engineer, eventhough I've now spent over 30+ years in Data Centers.<br>
&ensp;&ensp;Data Center Design Engineering is a complete field of study on to itself.<br>
Data Center Concerns and Issues:<br>
&ensp;&ensp;"Normal" deployed power density ranges from 5-6kW per rack,<br>
&ensp;&ensp;anything above that could be considered high density, up to around 30kW per rack.<br>
&ensp;&ensp;Some data centers exceed this, even achieving ultrahigh density of up to 50-60kW per rack.<br>
&ensp;&ensp;When it comes to data centers, more power in a smaller footprint equals more efficiency.<br>
&ensp;&ensp;In 2023, US data centers are expected to consume 100 billion kilowatt-hours of energy (100 GWh), according to one energy-usage report.<br>
&ensp;&ensp;As if that wasn't bad enough, each kilowatt-hour of energy requires two gallons of water to cool it.<br>
&ensp;&ensp;So for 2023 alone, that equates to some 250,000 Olympic-size swimming pools of water.<br>
&ensp;&ensp;[2023 Global Data Center Trends](https://www.cbre.com/insights/reports/global-data-center-trends-2023):<br>
&ensp;&ensp;Northern Virginia remains the world's largest data center market with [2,132 MW of total inventory](https://img.datacenterfrontier.com/files/base/ebm/datacenterfrontier/image/2023/10/Dominion_Data_Center_Dorecast_Through_2038.6526914266bfc.png?auto=format,compress&w=1500&h=843&cache=0.28452957888253116&fit=max) and growing.<br>
&ensp;&ensp;[The AI Disruption: Challenges and Guidance for Data Center Design](https://www.se.com/us/en/download/document/SPD_WP110_EN/) [[1]](https://download.schneider-electric.com/files?p_Doc_Ref=SPD_WP110_EN&p_enDocType=White+Paper&p_File_Name=WP110_V1.1_EN.pdf)<br>
&ensp;&ensp;[AI Data Center Energy Consumption](https://www.youtube.com/watch?v=wz6K9C6G5oA#t=00h13m34s)<br>
&ensp;&ensp;Data Centers account for 1.5% of global electricity use, which is 300TWh of energy per year<br>
&ensp;&ensp;which is about the energy consumption of the entire United Kingdom!<br>
Cloud Data Centers:<br>
&ensp;&ensp;[Azure Global Infrastructure](https://azure.microsoft.com/en-us/explore/global-infrastructure) is comprised of 300+ physical datacenters.<br>
&ensp;&ensp;[Facebook's](https://www.youtube.com/watch?v=hkT0QKDmCiY) largest data center houses more than 400,000 computer servers.<br>
&ensp;&ensp;[AWS Data Centers Today: 100+ Locations, 1.5 Million Servers, and More](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiPgJmE4vaBAxVaD0QIHTYPB-8QFnoECBMQAw&url=https%3A%2F%2Fwww.cloudzero.com%2Fblog%2Faws-data-center-locations&usg=AOvVaw00IBauiqtFxZ3jWJ3jOZFk&opi=89978449)<br>
&ensp;&ensp;AWS has over 100 data centers globally, covering 31 AWS Regions, 99 Availability Zones,<br>
&ensp;&ensp;over 400 edge locations/local zones, and 245 countries and territories.<br>
&ensp;&ensp;[AWS Cloud Infrastructure](https://www.youtube.com/watch?v=q6WlzHLxNKI)<br>
&ensp;&ensp;[Google Cloud’s Data Center Locations: Regions and Availability Zones](https://dgtlinfra.com/google-cloud-data-center-locations/) Google operates or is developing 35 data centers around the world.<br>
&ensp;&ensp;[Google Data Centers](https://www.google.com/about/datacenters/)<br>
&ensp;&ensp;[Google Cloud Infrastructure](https://cloud.google.com/infrastructure)<br>
&ensp;&ensp;[How does Google design its data centers?](https://www.youtube.com/watch?v=9IZ4qPAL-vA)<br>
Data Center Performance Tuning:<br>
&ensp;&ensp;48V DC for Data Center Devices: Routers, Switches, Servers, Load Balancers, etc.<br>
&ensp;&ensp;[It's Time to Replace TCP in the Datacenter](https://www.youtube.com/watch?v=o2HBHckrdQc) [[1]](https://arxiv.org/abs/2210.00714) [[2]](https://netdevconf.info/0x16/keynote/netdev0x16-keynote.pdf) [[3]](https://blog.ipspace.net/2023/01/data-center-tcp-replacement.html)<br>
&ensp;&ensp;[TCP Offload Engine (TOE)](https://en.wikipedia.org/wiki/TCP_offload_engine)<br>
&ensp;&ensp;[eBPF](https://en.wikipedia.org/wiki/EBPF) [[1]](https://ebpf.io/)<br>
&ensp;&ensp;[Protocol Buffers](https://en.wikipedia.org/wiki/Protocol_Buffers) [[1]](https://protobuf.dev/overview/) [[2]](https://github.com/protocolbuffers/protobuf)<br>
&ensp;&ensp;[gRPC](https://en.wikipedia.org/wiki/GRPC) [[1]](https://github.com/grpc/grpc) [[2]](https://grpc.io/docs/what-is-grpc/introduction/)<br>
Pick at least 3 Data Centers: (for redundancy)<br>
&ensp;&ensp;There are currently [four data center tiers](https://phoenixnap.com/blog/data-center-tiers-classification), [ranked by performance and uptime](https://www.impactmybiz.com/blog/data-center-tiers-explained/<).<br>
&ensp;&ensp;My Favorite Data Centers:<br>
&ensp;&ensp;&ensp;&ensp;1) [PheonixNAP](https://phoenixnap.com/)<br>
&ensp;&ensp;&ensp;&ensp;2) [SwitchNAP - Tahoe](https://www.switch.com/tahoe-reno/)<br>
&ensp;&ensp;&ensp;&ensp;3) [SwitchNAP - Las Vegas](https://www.switch.com/las-vegas/) [[1]](https://www.switch.com/locations/)<br>
&ensp;&ensp;&ensp;&ensp;4) [SwitchNAP - Grand Rapids](https://www.switch.com/grand-rapids/)<br>
&ensp;&ensp;&ensp;&ensp;5) [SwitchNAP - Atlanta](https://www.switch.com/atlanta/)<br>
&ensp;&ensp;&ensp;&ensp;6) [SwitchNAP - Austin](https://www.switch.com/switch-announces-fifth-prime-expansion-with-development-of-exascale-data-center-campus-in-texas/)<br>
&ensp;&ensp;Purchase equipment (routers, switches, servers, loadbalancers, Firewalls, etc.).<br>
&ensp;&ensp;Ship Equipment to Data Centers.<br>
&ensp;&ensp;Rack and Cable all the equipment: Power, Network, Out-of-band Access: [IPMI:](https://en.wikipedia.org/wiki/Intelligent_Platform_Management_Interface) [Dell iDRAC](https://en.wikipedia.org/wiki/Dell_DRAC), [HP iLO](https://en.wikipedia.org/wiki/HP_Integrated_Lights-Out), etc.<br>
&ensp;&ensp;Configure WAN BGP Peering Connections on your Border Routers - aka., Connect your Data Center to the Internet and other Data Centers.<br>
&ensp;&ensp;Create and Deploy LAN Network Design: Valley-free Routing vs. Leaf and Spine Topology, LAG and/or MLAG, etc.<br>
&ensp;&ensp;Install OS or Type-1 Hypervisor on all baremetal machines with [Bootstrap Tools:](https://en.wikipedia.org/wiki/Bootstrapping_(disambiguation)) [cloud-init](https://cloud-init.io/)/[cloud-init Github](https://github.com/canonical/cloud-init), [iPXE](https://en.wikipedia.org/wiki/IPXE), [ipmitool](https://github.com/ipmitool/ipmitool)/[ipmiutil](https://github.com/arcress0/ipmiutil), [Tinkerbell](https://tinkerbell.org/), [Shoelaces](https://github.com/thousandeyes/shoelaces), [Redfish](https://dmtf.github.io/python-redfish-utility/#overview)/[RedfishTool](https://github.com/DMTF/Redfishtool), etc.<br>
&ensp;&ensp;Configure all servers with your [Provisioning Tools:](https://en.wikipedia.org/wiki/Category:Orchestration_software) [Ansible](https://en.wikipedia.org/wiki/Ansible_(software)), [Terraform](https://en.wikipedia.org/wiki/Terraform_(software)), [Pulumi](https://en.wikipedia.org/wiki/Pulumi); [Package Managers:](https://en.wikipedia.org/wiki/List_of_software_package_management_systems) [DNF](https://en.wikipedia.org/wiki/DNF_(software))/[RPM](https://en.wikipedia.org/wiki/RPM_Package_Manager), [APT](https://en.wikipedia.org/wiki/APT_(software))/[DPKG](https://en.wikipedia.org/wiki/Dpkg), [Pacman](https://en.wikipedia.org/wiki/Arch_Linux#Pacman), [OSTree](https://en.wikipedia.org/wiki/OSTree); [Firmware Installers:](https://en.wikipedia.org/wiki/Firmware) [fwupd](https://en.wikipedia.org/wiki/Fwupd), [flash-kernel](https://packages.debian.org/flash-kernel), [flashrom](https://packages.debian.org/flashrom), [grub-imageboot](https://packages.debian.org/grub-imageboot), [FlashBIOS](https://wiki.debian.org/FlashBIOS), [grml2usb](https://packages.debian.org/grml2usb), [openseachest](https://packages.debian.org/openseachest)<br>
&ensp;&ensp;Create VMs and/or Containers on your servers.<br>
&ensp;&ensp;Install Container Orchestration Software on baremetal or VMs: Kubernetes et.al.<br>
&ensp;&ensp;Design Kubernetes System Design to best support your workload.<br>
&ensp;&ensp;Deploy applications on Kubernetes cluster.<br>
&ensp;&ensp;Maintain everything!<br>
&ensp;&ensp;Have Fun!<br>
&ensp;&ensp;Make Money!<br>
Aquire and Configure all non-hardware Internet Related Resources to get you up and running.<br>
&ensp;&ensp;This short list includes:<br>
&ensp;&ensp;aquiring an ASN, [CIDR Blocks](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing), establishing BGP Peering, configure BGP [Anycast](https://en.wikipedia.org/wiki/Anycast), create and implement WAN design<br>
&ensp;&ensp;Again, the details of doing even this short list took me 30+ years to perfect.<br>
&ensp;&ensp;Network Engineering is a complete field of study on to itself.<br>
Aquire [ASN](https://en.wikipedia.org/wiki/Autonomous_system_(Internet)) from [ARIN](https://en.wikipedia.org/wiki/American_Registry_for_Internet_Numbers):<br>
&ensp;&ensp;All resource requests require an [ARIN](https://en.wikipedia.org/wiki/American_Registry_for_Internet_Numbers) Online account linked to either an Admin or Tech [Point of Contact (POC)](https://www.arin.net/resources/guide/account/records/poc/) [[1]](https://en.wikipedia.org/wiki/Point_of_contact) record<br>
&ensp;&ensp;with the authority to request resources for a valid [Organization Identifier (Org ID)](https://www.arin.net/resources/guide/account/records/org/).<br>
&ensp;&ensp;https://www.arin.net/resources/guide/quickguide.pdf<br>
&ensp;&ensp;https://www.arin.net/blog/2019/09/24/how-to-request-an-asn-from-arin/<br>
&ensp;&ensp;https://ipinfo.io/<ASN><br>
&ensp;&ensp;https://mxtoolbox.com/asn.aspx<br>
&ensp;&ensp;http://navigators.com/isp.html<br>
&ensp;&ensp;https://www.peeringdb.com/<br>
  Aquire from [ARIN](https://en.wikipedia.org/wiki/American_Registry_for_Internet_Numbers) IP [CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing) Block/Addresses (IPv4 or IPv6) - IPv6 is preferred!<br>
&ensp;&ensp;https://www.youtube.com/watch?v=nCm6bLPh-Pw#t=00h00m00s?=#- Using Your ARIN Online Account - Requesting IP Address Space<br>
&ensp;&ensp;https://www.arin.net/resources/guide/request/<br>
&ensp;&ensp;https://www.arin.net/resources/guide/ipv4/request/<br>
&ensp;&ensp;https://www.arin.net/resources/guide/ipv6/<br>
&ensp;&ensp;https://www.arin.net/resources/guide/ipv6/first_request/<br>
&ensp;&ensp;https://www.arin.net/resources/guide/ipv6/preparing_apps_for_v6.pdf<br>
&ensp;&ensp;https://www.arin.net/reference/materials/cidr.pdf<br>
&ensp;&ensp;https://mxtoolbox.com/arin.aspx<br>
&ensp;&ensp;https://datatracker.ietf.org/doc/html/rfc4632<br>
&ensp;&ensp;http://www.cidr-report.org/as2.0<br>
&ensp;&ensp;https://bgp.potaroo.net/index-cidr.html<br>
&ensp;&ensp;https://ip2cidr.com/<br>
&ensp;&ensp;https://whoisrequest.com/<br>
BGP: (iBGP,eBGP)<br>
&ensp;&ensp;Establish BGP peering relationship, aka., Connect your Data Center to the Internet.<br>
&ensp;&ensp;Implement your WAN Design to connect all your Datacenters together.<br>
&ensp;&ensp;Configure BGP [Anycast](https://en.wikipedia.org/wiki/Anycast) to connect your customers to all of your Data Centers.<br>
&ensp;&ensp;For static data, use Edge Networking or CDNs to improve latency for your customers.<br>
&ensp;&ensp;For dynamic data, include a Caching layer to improve latency for your customers.<br>
BGP Tools:<br>
&ensp;&ensp;https://bgplay.massimocandela.com/<br>
&ensp;&ensp;https://github.com/massimocandela/BGPlay<br>
&ensp;&ensp;https://lookinglass.org/<br>
&ensp;&ensp;https://www.bgp4.as/looking-glasses<br>
&ensp;&ensp;https://bgpview.io/<br>
&ensp;&ensp;https://bgp.potaroo.net/index-bgp.html<br>
&ensp;&ensp;https://github.com/irrtoolset/irrtoolset<br>
IPv4:<br>
&ensp;&ensp;RFC1918: Non-Routable IPv4 Networks/Addresses<br>
IPv4 Tools:<br>
&ensp;&ensp;[MXToolBox Network Tools](https://mxtoolbox.com/NetworkTools.aspx)<br>
&ensp;&ensp;[MXToolBox Subnet Calculator](https://mxtoolbox.com/subnetcalculator.aspx)<br>
&ensp;&ensp;Display arp cache: aka., MAC Addresses<br>
&ensp;&ensp;# arp -a<br>
&ensp;&ensp;Display IP Addressess:<br>
&ensp;&ensp;# ip a | grep inet | grep -v inet6 | grep -v 127.0.0.0<br>
&ensp;&ensp;Display Routing Table and Default Gateway<br>
&ensp;&ensp;# ip r<br>
&ensp;&ensp;Display open TCP and UDP Ports on your host<br>
&ensp;&ensp;# nmap -sU <ip-address><br>
&ensp;&ensp;# nmap -Pn <ip-address><br>
IPv6:<br>
IPv6 has two Internal address types:<br>
&ensp;&ensp;1) Link Local:<br>
&ensp;&ensp;&ensp;&ensp;Link local addresses are not routed on the Internal network or the Internet.<br>
&ensp;&ensp;&ensp;&ensp;Link local addresses start with fe80<br>
&ensp;&ensp;&ensp;&ensp;Link Local addresses are self assigned i.e. they do not require a DHCP server.<br>
&ensp;&ensp;&ensp;&ensp;A link local address is required on every IP6 interface even if no routing is present.<br>
&ensp;&ensp;2) Unique Local:<br>
&ensp;&ensp;&ensp;&ensp;Unique Local addresses are meant to be used inside an internal network.<br>
&ensp;&ensp;&ensp;&ensp;Unique Local addresses are equivalent to RFC1918 addresses.<br>
&ensp;&ensp;&ensp;&ensp;The address space is divided into two /8 spaces: fc00::/8 for globally assigned addressing, and fd00::/8 for locally assigned addressing.<br>
&ensp;&ensp;&ensp;&ensp;[RFC4193: Unique Local IPv6 Unicast Addresses](https://datatracker.ietf.org/doc/html/rfc4193)<br>
&ensp;&ensp;&ensp;&ensp;[IPv6 Address Types](https://www.ripe.net/manage-ips-and-asns/ipv6/ipv6-address-types/ipv6addresstypes.pdf)<br>
&ensp;&ensp;&ensp;&ensp;[IPv4/IPv6 dual-stack](https://kubernetes.io/docs/concepts/services-networking/dual-stack/)<br>
&ensp;&ensp;&ensp;&ensp;[Validate IPv4/IPv6 dual-stack](https://kubernetes.io/docs/tasks/network/validate-dual-stack/)<br>
&ensp;&ensp;&ensp;&ensp;[Tutorial: Assigning IPv6 addresses to Kubernetes Pods and services](https://docs.aws.amazon.com/eks/latest/userguide/cni-ipv6.htm)<br>
&ensp;&ensp;&ensp;&ensp;[What the Arrival of IPv6 Support in Kubernetes Means for You](https://deploy.equinix.com/blog/kubernetes-ipv6-ipv4-dual-stack-networking/)<br>
IPv6 Tools:<br>
&ensp;&ensp;&ensp;&ensp;[Free IPv6 Tools](http://www.ipamworldwide.com/libraries/toolmenu.html)<br>
&ensp;&ensp;&ensp;&ensp;[MXToolBox Network Tools](https://mxtoolbox.com/NetworkTools.aspx)<br>
Register Domain Names:<br>
&ensp;&ensp;There are several Domain Registrars:<br>
&ensp;&ensp;https://www.bluehost.com/domains<br>
&ensp;&ensp;https://www.godaddy.com/domains<br>
Install and Configure certbot (aka., LetsEncrypt)<br>
&ensp;&ensp;Let's Encrypt is a global Certificate Authority (CA).<br>
&ensp;&ensp;Certbot lets people and organizations around the world<br>
&ensp;&ensp;obtain, renew, and manage SSL/TLS certificates.<br>
&ensp;&ensp;Certbot certificates can be used by websites to enable secure HTTPS connections.<br>
&ensp;&ensp;Certbot certifactes are free!<br>
&ensp;&ensp;https://letsencrypt.org/docs/faq/<br>
&ensp;&ensp;https://letsencrypt.org/getting-started/<br>
&ensp;&ensp;https://github.com/letsencrypt/website/<br>
&ensp;&ensp;https://letsencrypt.org/documents/isrg-cps-v3.0/<br>
&ensp;&ensp;https://letsencrypt.org/docs/client-options/<br>
Network Time Protocol (NTP):<br>
&ensp;&ensp;If your time is off on your servers, then your logs will be off<br>
&ensp;&ensp;and other applications will also start to fail!<br>
&ensp;&ensp;NTP gives client synchronization accuracies in the millisecond range.<br>
&ensp;&ensp;I use NTPsec:<br>
&ensp;&ensp;$ dnf install -y ntpsec<br>
&ensp;&ensp;ftp://ftp.ntpsec.org/pub/releases/ntpsec-1.1.8.tar.gz<br>
&ensp;&ensp;https://www.ntpsec.org/<br>
&ensp;&ensp;https://docs.ntpsec.org/latest/NTS-QuickStart.html<br>
&ensp;&ensp;https://docs.ntpsec.org/latest/build.html#unix<br>
&ensp;&ensp;https://github.com/ntpsec/ntpsec<br>
&ensp;&ensp;https://github.com/ntpsec/ntpsec.github.io<br>
&ensp;&ensp;https://gitlab.com/NTPsec<br>
&ensp;&ensp;https://gitlab.com/NTPsec/ntpsec/blob/master/devel/nts.adoc<br>
&ensp;&ensp;https://weberblog.net/setting-up-nts-secured-ntp-with-ntpsec/<br>
&ensp;&ensp;$ cat /etc/ntpsec/ntp.conf<br>
&ensp;&ensp;$ hwclock --show<br>
&ensp;&ensp;$ timedatectl status<br>
&ensp;&ensp;$ ntpdate -q us.pool.ntp.org<br>
&ensp;&ensp;$ ntpdate -q 0.pool.ntp.org<br>
&ensp;&ensp;$ ntpq -p<br>
&ensp;&ensp;$ ntpq -c rv<br>
&ensp;&ensp;[Computer Network Time Synchronization](https://www.eecis.udel.edu/~mills/book.html)<br>
&ensp;&ensp;[Open Time Server](http://www.opentimeserver.com/)<br>
&ensp;&ensp;[Open Time Server on Github](https://github.com/opencomputeproject/Time-Appliance-Project/tree/master/Open-Time-Server)<br>
&ensp;&ensp;[Google Public NTP](https://developers.google.com/time)<br>
&ensp;&ensp;[Cloudflare Time Services](https://time.cloudflare.com/)<br>
&ensp;&ensp;time-services@cloudflare.com<br>
&ensp;&ensp;https://www.cloudflare.com/time/<br>
&ensp;&ensp;[NIST Internet Time Servers](https://tf.nist.gov/tf-cgi/servers.cgi)<br>
&ensp;&ensp;[NTP Pool Project](https://www.ntppool.org/en/)<br>
Precision Time Protocol: (PPT) IEEE 1588<br>
&ensp;&ensp;PPT gives slave synchronization accuracies in the nanosecond or microsecond range.<br>
&ensp;&ensp;https://en.wikipedia.org/wiki/Precision_Time_Protocol<br>
&ensp;&ensp;https://en.wikipedia.org/wiki/IEEE_1588<br>
&ensp;&ensp;https://www.nist.gov/el/intelligent-systems-division-73500/ieee-1588<br>
&ensp;&ensp;https://linuxptp.sourceforge.net/<br>
DNS: ISC-BIND (stable versions are even release numbers)<br>
&ensp;&ensp;Kubernetes uses CoreDNS for DNS resolution amoung their Pods.<br>
&ensp;&ensp;I use ISC-BIND for the Baremetal and VMs underneath Kubernetes.<br>
&ensp;&ensp;Public DNS: 1.1.1.1, 8.8.8.8, 8.8.4.4, 9.9.9.9<br>
&ensp;&ensp;https://www.isc.org/bind/<br>
&ensp;&ensp;https://downloads.isc.org/isc/bind9/cur/<br>
&ensp;&ensp;https://downloads.isc.org/isc/bind9/cur/9.18/doc/arm/Bv9ARM.pdf<br>
DNSSEC:<br>
&ensp;&ensp;DNSSEC - What Is It and Why Is It Important?<br>
&ensp;&ensp;https://www.icann.org/resources/pages/dnssec-what-is-it-why-important-2019-03-05-en<br>
&ensp;&ensp;[DNSSEC Basics](https://www.internetsociety.org/deploy360/dnssec/basics/)<br>
&ensp;&ensp;[DNSSEC Overview](https://www.youtube.com/watch?v=MrtsKTC3KDM)<br>
&ensp;&ensp;[DNSSec Explained](https://www.youtube.com/watch?v=_8M_vuFcdZU)<br>
DNS Tools:<br>
&ensp;&ensp;Stork is a dashboard for BIND 9 and Kea DHCP:<br>
&ensp;&ensp;https://gitlab.isc.org/isc-projects/stork<br>
&ensp;&ensp;$ man dig<br>
&ensp;&ensp;$ man mdig<br>
&ensp;&ensp;$ man delv<br>
&ensp;&ensp;$ nmap --script broadcast-dhcp-discover -e <nic-interface><br>
&ensp;&ensp;https://www.isc.org/dns-tools/<br>
&ensp;&ensp;https://who.is/<br>
&ensp;&ensp;https://dnschecker.org/<br>
&ensp;&ensp;https://www.dnswatch.info/<br>
&ensp;&ensp;http://www.mavetju.org/download/dnstracer-1.9.tar.gz<br>
DNS Root Servers:<br>
&ensp;&ensp;https://www.iana.org/domains/root/servers<br>
&ensp;&ensp;https://www.internic.net/domain/root.zone<br>
&ensp;&ensp;https://root-servers.org/<br>
DHCP: ISC-KEA (replaces ISC-DHCP)<br>
&ensp;&ensp;https://www.isc.org/kea/<br>
&ensp;&ensp;https://gitlab.isc.org/isc-projects/kea<br>
&ensp;&ensp;https://kea.readthedocs.io/en/latest/<br>
DHCP Tools:<br>
&ensp;&ensp;Stork is a dashboard for BIND 9 and Kea DHCP:<br>
&ensp;&ensp;https://gitlab.isc.org/isc-projects/stork<br>
&ensp;&ensp;https://www.isc.org/kea-tools/<br>
&ensp;&ensp;https://www.isc.org/dhcp-tools/ <-- ISC announced the end of maintenance for ISC DHCP as of the end of 2022 - use Kea instead!<br>
&ensp;&ensp;http://www.mavetju.org/download/dhcping-1.2.tar.gz<br>
&ensp;&ensp;http://www.mavetju.org/download/dhcpdump-1.8.tar.gz<br>
Configure Out-of-band Access to all Servers:<br>
&ensp;&ensp;IPMI: Dell iDRAC, HP iLO<br>
&ensp;&ensp;# dnf install ipmitool ipmiutil<br>
&ensp;&ensp;Discover all ipmi servers on your network:<br>
&ensp;&ensp;# ipmiutil discover<br>
Find your NAT IP:<br>
&ensp;&ensp;https://www.ipchicken.com/<br>
&ensp;&ensp;# curl ifconfig.me<br>
&ensp;&ensp;# tranceroute .net<br>

## OnPrem Tools
&ensp;&ensp;[OpenSSH](https://en.wikipedia.org/wiki/OpenSSH) [[1]](https://www.openssh.com/) [[2]](https://github.com/openssh/openssh-portable)<br>
&ensp;&ensp;[sshpass](https://github.com/kevinburke/sshpass) [[1]](https://www.cyberciti.biz/faq/noninteractive-shell-script-ssh-password-provider/) [[2]](https://www.redhat.com/sysadmin/ssh-automation-sshpass) [[3]](https://medium.com/linuxstories/how-to-ssh-copy-id-multiple-hosts-using-xargs-and-sshpass-8935737c24b)<br>
&ensp;&ensp;[Keychain](https://www.funtoo.org/Funtoo:Keychain) [[1]](https://github.com/funtoo/keychain) [[2]](https://github.com/funtoo/keychain/releases) [[3]](https://unix.stackexchange.com/questions/605177/funtoo-keychain-keeps-asking-for-password-when-logging-in-using-ssh) [[4]](https://helpmanual.io/help/keychain/) [[5]](https://stackoverflow.com/questions/64847022/git-integrate-with-funtoo-keychain) [[6]](https://www.cyberciti.biz/faq/ubuntu-debian-linux-server-install-keychain-apt-get-command/)<br>
&ensp;&ensp;[Assh](https://github.com/moul/assh) [[1]](https://github.com/moul/assh/releases) [[2]](https://medium.com/passion-madness/assh-2974cf23c7be) [[3]](https://developpaper.com/use-assh-to-manage-ssh-config/) [[4]](https://manfred.life/assh)<br>
&ensp;&ensp;[Mosh](https://en.wikipedia.org/wiki/Mosh_(software)) [[1]](https://mosh.org/) [[2]](https://github.com/mobile-shell/mosh) [[3]](https://www.engagespark.com/blog/mosh-through-firewalls/) [[4]](https://github.com/carltonf/mosh-via-tunnel)<br>
&ensp;&ensp;[Tmux](https://en.wikipedia.org/wiki/Tmux) [[1]](https://github.com/tmux/tmux/wiki) [[2]](https://github.com/tmux-plugins/tpm) [[3]](https://github.com/catppuccin/tmux) [[4]](https://github.com/wenijinew/eutmux) [[5]](https://tmuxp.git-pull.com/index.html) [[6]](https://medium.com/code-art/after-n-years-im-finally-using-tmux-in-such-an-elegant-way-8d2492d964db) [[7]](https://www.youtube.com/watch?v=DzNmUNvnB04)<br>
&ensp;&ensp;[GNU Screen](https://en.wikipedia.org/wiki/GNU_Screen) [[1]](https://www.gnu.org/software/screen/) [[2]](https://git.savannah.gnu.org/cgit/screen.git)<br>
&ensp;&ensp;[Wireguard:](https://en.wikipedia.org/wiki/WireGuard) [Installing WireGuard-UI to Manage Your WireGuard VPN Server](https://insights.ditatompel.com/en/tutorials/installing-wireguard-ui-to-manage-your-wireguard-vpn-server/) [[1]](https://www.wireguard.com/) [[2]](https://git.zx2c4.com/wireguard-linux) [[3]](https://www.wireguard.com/repositories/) [[4]](https://www.wireguard.com/quickstart/) [[5]](https://www.freecodecamp.org/news/build-your-own-wireguard-vpn-in-five-minutes/) [[6]](https://superuser.com/questions/1770829/how-to-setup-a-vpn-tunnel-using-wireguard) [[7]](https://upcloud.com/resources/tutorials/get-started-wireguard-vpn) [[8]](https://docs.opnsense.org/manual/how-tos/wireguard-client.html) [[9]](https://www.asus.com/support/FAQ/1048280/) [[10]](https://wiki.archlinux.org/title/WireGuard) [[11]](https://www.ivpn.net/setup/linux-wireguard/) [[12]](https://www.techrepublic.com/videos/how-to-install-and-configure-wireguard-vpn-on-linux/) [[13]](https://fedoramagazine.org/configure-wireguard-vpns-with-networkmanager/) [[14]](https://docs.fedoraproject.org/en-US/fedora-coreos/sysconfig-configure-wireguard/) [[15]](https://two-oes.medium.com/wireguard-as-a-vpn-solution-for-home-connection-b79e2812baa2) [[16]](https://bash-prompt.net/guides/wireguard-setup/) [[17]](https://www.youtube.com/watch?v=SMF301vQqJo) [[18]](https://github.com/pirate/wireguard-docs)<br>
&ensp;&ensp;[Bitwarden:](https://en.wikipedia.org/wiki/Bitwarden) [Login to Bitwarden](https://vault.bitwarden.com/#/login) [BitWarden Youtube Channel](https://www.youtube.com/@Bitwarden/videos) [[1]](https://bitwarden.com/) [[2]](https://github.com/bitwarden) [[3]](https://bitwarden.com/help/install-on-premise-linux/) [[4]](https://bitwarden.com/help/install-on-premise-manual/) [[5]](https://mshelton.medium.com/bitwarden-for-beginners-74cf93679457) [[6]](https://bitwarden.com/learning/getting-started-password-manager/)<br>
&ensp;&ensp;[Jitsi](https://jitsi.org/) [Jitsi Github](https://github.com/jitsi) [Jitsi Github](https://github.com/jitsi/jitsi) [Jitsi Meet](https://meet.jit.si/) [Jitsi Meet Github](https://github.com/jitsi/jitsi-meet) [Moderated Jitsi](https://moderated.jitsi.net/) [Jitsi Youtube Channel](https://www.youtube.com/@JitsiOrg/videos) [[1]](https://en.wikipedia.org/wiki/Jitsi) [[2]](https://desktop.jitsi.org/) [[3]](https://jitsi.github.io/handbook/docs/intro/) [[4]](https://chrome.google.com/webstore/detail/jitsi-meetings/kglhbbefdnlheedjiejgomgmfplipfeb) [[5]](https://twitter.com/jitsinews?lang=en) [[6]](https://www.linode.com/marketplace/apps/linode/jitsi/) [[7]](https://www.facebook.com/jitsi/) [[8]](https://www.techradar.com/reviews/jitsi-meet-review) [[9]](https://docs.fedoraproject.org/en-US/quick-docs/jitsi-getting-started/) [[10]](https://marketplace.digitalocean.com/apps/jitsi-server) [[11]](https://www.infoq.com/articles/mobile-video-conferencing-jitsi/) [[12]](https://aws.amazon.com/marketplace/pp/prodview-bwqjrqw6grhjs) [[13]](https://summerofcode.withgoogle.com/archive/2022/organizations/jitsi) [[14]](https://itsfoss.com/jitsi-meet/) [[15]](https://platform.physik.kit.edu/en/article/jitsi/) [[15]](https://wiki.archlinux.org/title/jitsi-meet) [[16]](https://aosabook.org/en/v1/jitsi.html) [[17]](https://groups.google.com/g/sandstorm-dev/c/M7fwUnLMi_g?pli=1) [[18]](https://foundation.mozilla.org/en/privacynotincluded/jitsimeet/)<br>
&ensp;&ensp;[Google Statistics](https://www.google.com/intl/en/ipv6/statistics.html)<br>
&ensp;&ensp;[Google Trending Page](https://trends.google.com/trends/)<br>
&ensp;&ensp;[Basics of Google Trends](https://newsinitiative.withgoogle.com/resources/trainings/basics-of-google-trends/)<br>
&ensp;&ensp;[Google Trends: See what's trending across Google Search, Google News and YouTube](https://newsinitiative.withgoogle.com/resources/trainings/google-trends-lesson/)<br>
&ensp;&ensp;[Github Trending Page](https://github.com/trending)<br>
&ensp;&ensp;https://time.is/<br>
&ensp;&ensp;http://www.convertunits.com/dates/from/Jan+1,+2023/to/Sep+28,+2023<br>
&ensp;&ensp;https://thetruesize.com/<br>

## My Favorite Hardware/Software for OnPrem Network, Compute and Storage
NOTE: These are my favorites but there are numerous other valid choices out there.<br>
Network Hardware:<br>
[List of Network Buses](https://en.wikipedia.org/wiki/List_of_network_buses)<br>
&ensp;&ensp;NOTE:<br>
&ensp;&ensp;&ensp;&ensp;I'm not including hardware Load Balancers or Firewalls because I prefer<br>
&ensp;&ensp;&ensp;&ensp;using the built-in software load balancing and security features of Kubernetes and all of<br>
&ensp;&ensp;&ensp;&ensp;the Kubernetes 3rd party options for distributing data and securing a cluster.<br>
&ensp;&ensp;&ensp;&ensp;In addition, I like using [BGP Anycast](https://en.wikipedia.org/wiki/Anycast) for WAN routing customers to the different data centers.<br>
&ensp;&ensp;Routers:<br>
&ensp;&ensp;&ensp;&ensp;Juniper:<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;I prefer Juniper JunOS over Cisco IOS.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[Juniper Routers](https://www.juniper.net/us/en/products/routers.html)<br>
&ensp;&ensp;&ensp;&ensp;Cisco:<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[All Cisco Routers Products](https://www.cisco.com/c/en/us/products/routers/product-listing.html)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[Cisco Routers](https://www.cisco.com/c/en_my/products/routers/index.html)<br>
&ensp;&ensp;&ensp;&ensp;FRR:<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;An inexpensive alternative would be to use a powerful Linux server with 100Gb NICs and FRR software.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;The only issue is FRR doesn't support MLAG which is a critical protocol for configuring redundancy.<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[FRRouting](https://en.wikipedia.org/wiki/FRRouting)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;https://github.com/FRRouting/frr<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;https://frrouting.org/<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;https://docs.frrouting.org/en/stable-9.0/<br>
&ensp;&ensp;Switches:<br>
&ensp;&ensp;&ensp;&ensp;[Edgecore](https://www.edge-core.com/productsList.php?cls=291&cls2=327)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[100Gb Switches](https://www.edge-core.com/productsList.php?cls=1&cls2=5)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[AS7816-64X: 64 ports 100G QSFP28](https://www.edge-core.com/productsInfo.php?cls=1&cls2=5&cls3=166&id=309)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[AS7726-32X: 32 ports 100G QSFP28, 2 x 10G SFP](https://www.edge-core.com/productsInfo.php?cls=&cls2=&cls3=15&id=545)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[10Gb Switches](https://www.edge-core.com/productsList.php?cls=1&cls2=154)<br>
&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;[Edgecore AS5912-54X: 48 ports 10G + 6 ports 100G](https://www.edge-core.com/productsInfo.php?cls=291&cls2=327&cls3=328&id=264)<br>
&ensp;&ensp;Fiber NICs:<br>
&ensp;&ensp;&ensp;&ensp;[10Gb SFP+ PCI-E Network Card NIC, with Broadcom BCM57810S Chip, Dual SFP+ Port, PCI Express X8](https://www.amazon.com/Ethernet-Broadcom-BCM57810S-Controller-Interface/dp/B06X9T683K?th=1)<br>
&ensp;&ensp;&ensp;&ensp;[100GbE Intel Ethernet Network Adapter E810](https://www.intel.com/content/www/us/en/products/details/ethernet/800-network-adapters/e810-network-adapters/products.html)<br>
&ensp;&ensp;&ensp;&ensp;[Deliver High-Performance Networking on Ethernet ](https://www.intel.com/content/www/us/en/content-details/787658/deliver-high-performance-networking-on-ethernet.html)<br>
Baremetal Servers:<br>
&ensp;&ensp;[List of Computer Buses](https://en.wikipedia.org/wiki/Category:Computer_buses)<br>
&ensp;&ensp;[List of Interface Bit Rates](https://en.wikipedia.org/wiki/List_of_interface_bit_rates)<br>
&ensp;&ensp;The biggest bottlenecks for computation are the "[Memory Wall](https://en.wikipedia.org/wiki/Random-access_memory#Memory_wall)" and the "[Von Neumann Bottleneck](https://en.wikipedia.org/wiki/Von_Neumann_architecture#Von_Neumann_bottleneck)".<br>
&ensp;&ensp;From 1986 to 2000, CPU speed improved at an annual rate of 55% while off-chip memory response time only improved at 10%.<br>
&ensp;&ensp;Given these trends, it was expected that memory latency would become an overwhelming bottleneck in computer performance.<br>
&ensp;&ensp;The other major problem is the [Power Problem](https://journal.uptimeinstitute.com/data-center-operators-will-face-more-grid-disturbances/).<br>
&ensp;&ensp;**According to McKinsey, U.S. data center power consumption is expected to reach 35 gigawatts by 2030.**<br>
&ensp;&ensp;[SuperStorage SSG-136R-NEL32JBF](https://www.supermicro.com/en/products/system/1U/136/SSG-136R-NEL32JBF.cfm)<br>
&ensp;&ensp;&ensp;&ensp;[32 32GB Hot-swap NVMe, 9.5mm EDSFF Long SSDs](https://www.supermicro.com/en/products/nvme) which is 1PB of storage capacity in 1U.<br>
&ensp;&ensp;&ensp;&ensp;[32 32GB Hot-swap E1.L SSD Server](https://www.facebook.com/Supermicro/videos/supermicro-superminute-e1l/378205252868226/)<br>
&ensp;&ensp;[Fujisu RX2540M7](https://www.fujitsu.com/global/products/computing/servers/primergy/rack/rx2540m7/index.html)<br>
&ensp;&ensp;&ensp;&ensp;2RU, dual-socket server with<br>
&ensp;&ensp;&ensp;&ensp;up to 60 Xeon cores per CPU,<br>
&ensp;&ensp;&ensp;&ensp;up to 8TB of DDR5 memory,<br>
&ensp;&ensp;&ensp;&ensp;PCIe gen 5 connectivity,<br>
&ensp;&ensp;&ensp;&ensp;up to 6x Nvidia GPUs,<br>
&ensp;&ensp;&ensp;&ensp;up to 24x 2.5-inch NVMe storage drives,<br>
&ensp;&ensp;&ensp;&ensp;and optionally six more at the rear of the chassis.<br>
[Storage Buses:]()<br>
&ensp;&ensp;[PCI Express (PCIe)](https://en.wikipedia.org/wiki/PCI_Express)<br>
&ensp;&ensp;&ensp;&ensp;PCIe 6.0  128 GB/s (PAM4)<br>
&ensp;&ensp;&ensp;&ensp;PCIe 5.0   64 GB/s (NRZ)<br>
&ensp;&ensp;&ensp;&ensp;PCIe 4.0   32 GB/s (2 GB/s/lane)<br>
&ensp;&ensp;&ensp;&ensp;PCIe 3.0   16 GB/s (1 GB/s/lane)<br>
Storage Devices: SSDs, HDDs<br>
&ensp;&ensp;I/O Bandwidth Doubles every 3 years - BUT latency lags behind See: "the [Memory Wall](https://en.wikipedia.org/wiki/Random-access_memory#Memory_wall)" problem.<br> 
&ensp;&ensp;1) [E1.L (Long) NVMe SSDs](https://www.intel.com/content/www/us/en/products/docs/memory-storage/solid-state-drives/edsff-brief.html)<br>
&ensp;&ensp;2) [Ultrastar DC HC670](https://www.westerndigital.com/products/internal-drives/data-center-drives/ultrastar-dc-hc670-hdd#ultrastar-dc-hc670-26-tb)<br>
&ensp;&ensp;&ensp;&ensp;26TB, 7200 RPM, 261MB/s<br>
Storage Software:<br>
&ensp;&ensp;1) Ceph:<br>
&ensp;&ensp;&ensp;&ensp;Supports object, block, and filesystem storage<br>
&ensp;&ensp;&ensp;&ensp;https://github.com/ceph/ceph<br>
&ensp;&ensp;&ensp;&ensp;https://ceph.com/<br>
&ensp;&ensp;&ensp;&ensp;https://github.com/ceph/ceph-csi<br>
&ensp;&ensp;2) Linstor:<br>
&ensp;&ensp;&ensp;&ensp;High performance block storage.<br>
&ensp;&ensp;&ensp;&ensp;https://github.com/piraeusdatastore/linstor-csi<br>
&ensp;&ensp;&ensp;&ensp;https://linbit.com/linstor/<br>
&ensp;&ensp;3) OpenEBS: aka., Maystor, based on SPDK<br>
&ensp;&ensp;&ensp;&ensp;Perfect for a database farm in Kubernetes.<br>
&ensp;&ensp;&ensp;&ensp;https://spdk.io/<br>
&ensp;&ensp;&ensp;&ensp;https://github.com/openebs/cstor-csi<br>
&ensp;&ensp;&ensp;&ensp;https://github.com/openebs/mayastor<br>
&ensp;&ensp;&ensp;&ensp;https://openebs.io/docs/concepts/mayastor<br>
&ensp;&ensp;&ensp;&ensp;https://mayastor.gitbook.io/introduction/<br>
&ensp;&ensp;&ensp;&ensp;https://percona.community/blog/2020/10/23/mayastor-lightning-fast-storage-for-kubernetes/<br>
&ensp;&ensp;&ensp;&ensp;https://blocksandfiles.com/2021/03/08/intel-says-mayastor-is-fastest-open-source-storage/<br>
&ensp;&ensp;4) Redis:<br>
&ensp;&ensp;&ensp;&ensp;Great for streaming applications.<br>
&ensp;&ensp;&ensp;&ensp;[Solving Concurrency Problems with Redis and Golang](https://blog.stackademic.com/solving-concurrency-problems-with-redis-and-golang-720e68b2b95a)<br>
&ensp;&ensp;5) RAMCloud:<br>
&ensp;&ensp;&ensp;&ensp;Great for streaming applications; very specialized; trying to get it to work with Kubernetes<br>
&ensp;&ensp;&ensp;&ensp;To achieve low latency, RAMCloud stores all data in DRAM at all times.<br>
&ensp;&ensp;&ensp;&ensp;https://github.com/PlatformLab/RAMCloud<br>
&ensp;&ensp;&ensp;&ensp;https://ramcloud.atlassian.net/wiki/spaces/RAM/overview<br>
&ensp;&ensp;&ensp;&ensp;https://ramcloud.atlassian.net/wiki/spaces/RAM/pages/6848537/Deciding+Whether+to+Use+RAMCloud<br>
&ensp;&ensp;&ensp;&ensp;https://web.stanford.edu/~ouster/cgi-bin/papers/ramcloud-tocs.pdf<br>

### Other System Design Resources
*) [ByteByteCode:](https://www.youtube.com/@ByteByteGo/videos)<br>
&ensp;&ensp;This Youtube channel is a great example of implementing "[Efficient Communication](https://github.com/Paul-J-Company/Systems-Design/edit/main/Systems-Design.md#design-principles)."<br>
&ensp;&ensp;[Data Replication: A Key Component for Building Large-Scale Distributed Systems](https://blog.bytebytego.com/p/data-replication-a-key-component)<br>
&ensp;&ensp;[The Most Beloved Burger for Developers](https://www.youtube.com/watch?v=7swoLEqABhQ)<br>
&ensp;&ensp;[10+ Key Memory & Storage Systems: Crash Course System Design #5](https://www.youtube.com/watch?v=lX4CrbXMsNQ)<br>
&ensp;&ensp;[10 Key Data Structures We Use Every Day](https://www.youtube.com/watch?v=ouipSd_5ivQ)<br>
&ensp;&ensp;[Top 7 Most-Used Distributed System Patterns](https://www.youtube.com/watch?v=nH4qjmP2KEE)<br>
&ensp;&ensp;[Latency Numbers Programmer Should Know](https://www.youtube.com/watch?v=FqR5vESuKe0)<br>
&ensp;&ensp;[What Are Microservices Really All About? (And When Not To Use It)](https://www.youtube.com/watch?v=lTAcCNbJ7KE)<br>
&ensp;&ensp;[Kubernetes Explained in 6 Minutes](https://www.youtube.com/watch?v=TlHvYWVUZyc)<br>
&ensp;&ensp;[CI/CD In 5 Minutes](https://www.youtube.com/watch?v=42UP1fxi2SY)<br>
&ensp;&ensp;[8 Key Data Structures That Power Modern Databases](https://www.youtube.com/watch?v=W_v05d_2RTo)<br>

*) [Be A Better Dev:](https://www.youtube.com/@BeABetterDev/videos)<br>
&ensp;&ensp;This Youtube Channel has several videos on AWS and are well made.<br>
&ensp;&ensp;[Intro to AWS - The Most Important Services To Learn](https://www.youtube.com/watch?v=FDEpdNdFglI)<br>
&ensp;&ensp;[Real Life AWS Project Architectures](https://www.youtube.com/watch?v=_W1xlhDsiAE)<br>
&ensp;&ensp;[Introduction to AWS | A Complete Beginner Roadmap](https://www.youtube.com/watch?v=lTyqzyk86f8)<br>
   
### Additional Resources
TBD
