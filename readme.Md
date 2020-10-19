1. A DDoS attack uses a tool, like a bot, that floods the network with signals over and over again, which eventually causes the network to stop being able to process genuine requests from users or other parts of the network. Web services and platforms are particularly at risk, as hackers can target critical services by overwhelming the network with traffic. DDoS attacks are often used against large businesses or banks; they can also cause problems with a business reputation if users do not know why a website or service is down. For these reasons, learning how to stop and prevent these attacks is crucial to business operations and success.

    To prevent ddos attacks :
    
    * we should have a plan as to what we are going to do when an attack happens, we should take care of all the vulnerabilities our system might have. We should strive to identify a ddos attack as early as possible
    
    * We should make sure we have appropriate protection tools installed for both your networks and your applications. This includes such key tools as firewalls, network monitoring software, anti-virus and anti-malware programs, as well as threat monitoring systems. With these, you can monitor your network baseline traffic and set up alerts for behavior that is out of the ordinary.
    

    * All these systems should be kept up to date, to make sure that any bugs or issues are fixed. Detecting threats as early as possible is the best way to prevent a DDoS attack from taking down important network infrastructures and affecting your end users.

    * One good way is to have more bandwidth available to our Web server than we need. That way, we can accommodate sudden and unexpected surges in traffic that could be a result of an advertising campaign, a special offer or even a mention of your company in the media.
   
    * Outsourcing DDoS prevention to cloud-based service providers offers several advantages. First, the cloud has far more bandwidth, and resources than a private network likely does. With the increased magnitude of DDoS attacks, relying solely on on-premises hardware is likely to fail.



2. Public ip address :
     
    This is the kind of IP address assigned to a device to enable access directly over the internet. Candidates for a public IP address can be an e-mail server, a web server, and similar systems which can be directly accessed from the internet. It is a globally unique IP address, which can be assigned to just one unique computing device.
    
   Private IP address : 

     A private IP address refers to the address space that is allocated by the Network Information Center to allow companies to form their own networks. There are class A, class B, and class C IP address blocks reserved for use in private environments. The computers, smartphones and tablets in your house and the PCs in an organization are often assigned different private IP addresses. Your network printer is being assigned a private IP address so that only you and your family members can print to that device. When a system is assigned an IP address, your local devices can see that PC via its private IP address. The devices residing beyond your local network, however, cannot communicate directly via the IP address, although they use your router’s address for this. To enable direct access to your local device that is assigned a private address, you have to use a Network Address Translator.
   

   Other common differences are:

   * Private IP address scope is local to present network whereAs public IP address scope is global.  
   * Private IP Addresses are free of cost whereas public IP Address comes with a cost.
   * Private IP Address starts somehwhat like 192.168...... where as Public IP Address is like 17.5.7.8
   * Private IP Addresses differ in a uniform manner whereAs public IP Addresses differ in varying range.
 



3. Active/passive Load Balancers:

   In a basic active/passive design, one controller (A) handles all traffic while the other (B) simply sits there waiting for its use. It comes to use when A suffers some kind of failure – and B then leaps into action, immediately replacing A by providing the same service. There might be a minor delay as the system performs a failover, but with multipathing software in place it will usually be quick enough to go unnoticed.
   

   Active/Active Load Balancers : 
   
   In an active/active architecture, both controllers (A and B) are available to handle traffic. This means that under normal operation you now have 2P of performance – and all for the same price . Both the overall performance and the price/performance have doubled.



   In active/passive design you are architecturally limited to seeing only 50% of your total available performance. For example, if we buy two controllers it means we have 2P of performance in our pocket, but we will forever be limited to a maximum of 1P of performance under this design.
    
   whereas,

   In active/active design, under normal operation we have 2P of performance. If controller A fails, we still have controller B functioning, which means we are now down to 1P of performance. It’s now half the performance we are used to in this architecture, but  that 1P is still the same performance as the active/passive model. The performance under failure is identical for both designs.

   In active/passive design, During failover, clients connect to the secondary companion to resubmit their uncommitted transactions. During failback, clients connect to the primary companion to resubmit their transactions. Clients with the failover property reestablish their connections automatically.
    
   whereAs,

   In active/active design, During failover and failback, clients connect to the same Adaptive Server to resubmit uncommitted transactions. Clients with the failover property reestablish their connections automatically.

   
   Taking cost into account,  building an active/passive system requires more expensive hardware than building a comparable active/active system. 

   Taking scalability into account, In an active/active design you have the option of adding more performance by adding more controllers. As long as your architecture supports the ability for all controllers to be active concurrently, adding performance is as simple as adding nodes into a cluster but  In an active/passive solution, You are architecturally limited to the performance of one controller. Adding more controllers just makes the price/performance even worse.
    



   
  


4.  The CAP theorem (also called Brewer’s theorem) states that a distributed database system can only guarantee two out of these three characteristics: Consistency, Availability, and Partition Tolerance.
    
    Consistency : 

     A system is said to be consistent if all nodes see the same data at the same time.

     Simply, if we perform a read operation on a consistent system, it should return the value of the most recent write operation. This means that, the read should cause all nodes to return the same data, i.e., the value of the most recent write.


    Availability :

    Availability in a distributed system ensures that the system remains operational 100% of the time. Every request gets a (non-error) response regardless of the individual state of a node.

    Note: this does not guarantee that the response contains the most recent write.
    

    Partition Tolerance:

    This condition states that the system does not fail, regardless of if messages are dropped or delayed between nodes in a system.

    Partition tolerance has become more of a necessity than an option in distributed systems. It is made possible by sufficiently replicating records across combinations of nodes and networks.
 

   No distributed system is safe from network failures, thus network partitioning generally has to be tolerated. In the presence of a partition, one is then left with two options: consistency or availability. When choosing consistency over availability, the system will return an error or a time out if particular information cannot be guaranteed to be up to date due to network partitioning. When choosing availability over consistency, the system will always process the query and try to return the most recent available version of the information, even if it cannot guarantee it is up to date due to network partitioning.

   In the absence of network failure – that is, when the distributed system is running normally – both availability and consistency can be satisfied.
   CAP is frequently misunderstood as if one has to choose to abandon one of the three guarantees at all times. In fact, the choice is really between consistency and availability only when a network partition or failure happens; at all other times, no trade-off has to be made






   Part 2 of the question :

   In my opinion, to Design database of https://university.attainu.com/ we should use mixture of relational database like MySQL, and Nosql databases like Mongodb.
    
   Both kinds of databases mentioned above have a set of advantages and disadvantages to their side, and we should use both to their advantages.
   
   For example, to store the information of students we should use relational database, such as MySQL because for data of students , a certain type of collection is linked to other type of collection, and it is easy to define relationships between information in a relational database system. 
   Taking example of a particular student, we need to store his basic info like name , roll no. , email id, and such and then performance of this student has to be linked with his basic info, suppose, the assignments submitted by him till now, his results in recent tests, this information has to be linked with students basic info, we can store both collections in two seperate tables and then join, or link both tables with his roll no or an id as the link between both collections.
   Now, suppose our Instructor, Manish Sir, wants to see how many students passed in a given test, so to achieve this we need to store results of all students for a particular test seperately,so we can make a collection for tests, and store their information about test, and id's(or roll no. of students) with their marks, which will make it easy to query. 
  

   below is a figure to show how tables can be formed and joined:
     ![alt text](https://media.geeksforgeeks.org/wp-content/uploads/20200508135718/Capture3231.png)
  
   Now, keeping in mind what we discussed above, we can take noSQL databases to our use as well, their are certain caveats with using just MySQL databases, as our data grows, the relationships become complex, and very hard to mantain and administor, so we need not to put every kind of collections in MySQL itself, for collections of data that we just need to store and deliver it to dashboard as fast as possible we can use NoSQL database like mongodb, NoSQL databases are fast as compared to MySQL. 
   
   We need not store other personal details of students in MySQL, like his work experience, his agreement information, his mentor's, TA's information, his cummalative test rank, his attendance, no. of sessions he has attended and such information which does not have complicated relationships between them, such information we need to just store, and play around, and deliver as quickly as possible and using NoSQL db like mongodb will come in great use in such case. 





5.
     1. SAR : UsedMonitor system real time performance (CPU, Memory, I/O, etc) , also used to  Collect performance data in the background on an on-going basis and do analysis on the historical data to identify bottlenecks.
     2. Tcpdump : tcpdump is a network packet analyzer. Using tcpdump you can capture the packets and analyze it for any performance bottlenecks.
     3. Top – Linux Process Monitoring : Linux Top command is a performance monitoring program which is used frequently by many system administrators to monitor Linux performance and it is available under many Linux/Unix like operating systems. The top command used to dipslay all the running and active real-time processes in ordered list and updates it regularly. It display CPU usage, Memory usage, Swap Memory, Cache Size, Buffer Size, Process PID, User, Commands and much more.
     4. VmStat – Virtual Memory Statistics : Linux VmStat command used to display statistics of virtual memory, kernerl threads, disks, system processes, I/O blocks, interrupts, CPU activity and much more. By default vmstat command is not available under Linux systems you need to install a package called sysstat that includes a vmstat program.
     5. Lsof – List Open Files : Lsof command used in many Linux/Unix like system that is used to display list of all the open files and the processes. The open files included are disk files, network sockets, pipes, devices and processes.
     6. Netstat – Network Statistics : Netstat is a command line tool for monitoring incoming and outgoing network packets statistics as well as interface statistics. It is very useful tool for every system administrator to monitor network performance and troubleshoot network related problems.
     7. uptime  : uptime command can be used to see how long the server has been running. The current time, how long the system has been running, how many users are currently logged on, and the system load averages for the past 1, 5, and 15 minutes.
     8. ps : ps command will report a snapshot of the current processes. To select all processes use the -A or -e option
     9. iostat : iostat command report Central Processing Unit (CPU) statistics and input/output statistics for devices, partitions and network filesystems (NFS).
     10.iptraf  : iptraf command is interactive colorful IP LAN monitor. It is an ncurses-based IP LAN monitor that generates various network statistics including TCP info, UDP counts, ICMP and OSPF information, Ethernet load info, node stats, IP checksum errors, and others.




6. The Master-Worker Pattern is used for parallel processing.

    It follows a simple approach that allows applications to perform simultaneous processing across multiple machines or processes via a Master and multiple Workers.
    
   In GigaSpaces data grid, you can implement the Master-Worker pattern using several methods:

    Task Executors - best for a scenario where the processing activity is collocated with the data (the data is stored within the same space as the tasks being executed).
    Polling Containers - in this case the processing activity runs in a separate machine/VM from the space. This approach should be used when the processing activity consumes a relatively large amount of CPU and takes a large amount of time. It might also be relevant if the actual data required for the processing is not stored within the space, or the time it takes to retrieve the required data from the space is much shorter than the time it takes to complete the processing.
   

    Suppose we want to batch process a number of small objects where object is data and large set of operations which could be performed to that object and we want to keep the object’s method list small, We can have a worker interface which defines the accessor API for the worker and how to add subjects where we can have multiple workers per subject and Our worker does the transformation, our subject is transformed.



7.
   * Round Robin is the preemptive process scheduling algorithm.

   * Each process is provided a fix time to execute, it is called a quantum.

   * Once a process is executed for a given time period, it is preempted and other process executes for a given time period.

   * Context switching is used to save states of preempted processes.


![alt text](https://media.geeksforgeeks.org/wp-content/uploads/round-robin-1.jpg)
 

  Cisco's IOS classic uses (or was) a non-preemptive round-robin scheduler.


8. Paging is a memory management scheme that eliminates the need for contiguous  allocation of physical memory. This scheme permits the physical address space of a process to be non – contiguous.

* Logical Address or Virtual Address (represented in bits): An address generated by the CPU
* Logical Address Space or Virtual Address Space( represented in words or bytes):   The set of all logical addresses generated by a program
 * Physical Address (represented in bits): An address actually available on memory unit
* Physical Address Space (represented in words or bytes): The set of all physical addresses corresponding to the logical addresses
Example:

If Logical Address = 31 bit, then Logical Address Space = 231 words = 2 G words (1 G = 230)
If Logical Address Space = 128 M words = 27 * 220 words, then Logical Address = log2 227 = 27 bits
If Physical Address = 22 bit, then Physical Address Space = 222 words = 4 M words (1 M = 220)
If Physical Address Space = 16 M words = 24 * 220 words, then Physical Address = log2 224 = 24 bits
The mapping from virtual to physical address is done by the memory management unit (MMU) which is a hardware device and this mapping is known as paging technique.

The Physical Address Space is conceptually divided into a number of fixed-size blocks, called frames.
The Logical address Space is also splitted into fixed-size blocks, called pages.
Page Size = Frame Size



9. A firewall is a network security device that monitors incoming and outgoing network traffic and permits or blocks data packets based on a set of security rules. Its purpose is to establish a barrier between your internal network and incoming traffic from external sources (such as the internet) in order to block malicious traffic like viruses and hackers.

* Next-generation firewalls (NGFW) combine traditional firewall technology with additional functionality, such as encrypted traffic inspection, intrusion prevention systems, anti-virus, and more. Most notably, it includes deep packet inspection (DPI). While basic firewalls only look at packet headers, deep packet inspection examines the data within the packet itself, enabling users to more effectively identify, categorize, or stop packets with malicious data. Learn about Forcepoint NGFW here.

* Proxy firewalls filter network traffic at the application level. Unlike basic firewalls, the proxy acts an intermediary between two end systems. The client must send a request to the firewall, where it is then evaluated against a set of security rules and then permitted or blocked. Most notably, proxy firewalls monitor traffic for layer 7 protocols such as HTTP and FTP, and use both stateful and deep packet inspection to detect malicious traffic.

 * Network address translation (NAT) firewalls allow multiple devices with independent network addresses to connect to the internet using a single IP address, keeping individual IP addresses hidden. As a result, attackers scanning a network for IP addresses can't capture specific details, providing greater security against attacks. NAT firewalls are similar to proxy firewalls in that they act as an intermediary between a group of computers and outside traffic.

* Stateful multilayer inspection (SMLI) firewalls filter packets at the network, transport, and application layers, comparing them against known trusted packets. Like NGFW firewalls, SMLI also examine the entire packet and only allow them to pass if they pass each layer individually. These firewalls examine packets to determine the state of the communication (thus the name) to ensure all initiated communication is only taking place with trusted sources.

10. Caching is the process of storing copies of files in a cache, or temporary storage location, so that they can be accessed more quickly. Technically, a cache is any temporary storage location for copies of files or data, but the term is often used in reference to Internet technologies. Web browsers cache HTML files, JavaScript, and images in order to load websites more quickly, while DNS servers cache DNS records for faster lookups and CDN servers cache content to reduce latency.

Cache is frequently used by cache clients, such as the CPU, applications, web browsers or operating systems (OSes). Cache is used because bulk, or main, storage can't keep up with the demands of the cache clients. Cache shortens data access times, reduces latency and improves input/output (I/O).