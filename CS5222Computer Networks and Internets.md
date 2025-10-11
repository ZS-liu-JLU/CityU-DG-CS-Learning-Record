***Lecture 1***

terminology(专门用语)

end system(端系统),host(主机),application(应用)

**Internet** : "networks of networks"

**Protocols** : control sending , receiving of messages

Internet standards : eg. RFC , IETF

**Network edge**

Internet structure（互联网结构） : 

-*Network edge* : 

hosts : clients and servers

servers in data centers

谢书中的边缘部分：由所有连接在互联网上的主机组成，用户直接使用的，用来进行通信和资源共享

-*Acess networks,physical media*

wired , wireless communication links 

-*Network core*

interconnected routers , network of networks

谢书中的核心部分：由大量网络和连接这些网络的路由器组成，这部分是为边缘部分提供服务的

Acess networks(接入网络) and physical media(物理介质)

-How to connect end systems to edge router?

*residential access nets ;*institutional acess networks(school,company);mobile access networks(WiFi,4G/5G)

-What to look for : 

*transmission rate (bits per second) of acess network? 

*shared or dedicated acess among users?

Host : sends packets of data

transmission delay = length of packets / transmission rate  
发送时延(传输时延)=数据帧长度/发送速率  
区分propagation delay(传播时延)

**Network core**  
--mesh of interconnected routers(互联的路由器)  
packeting-switching(分组交换) : hosts split application-layer messages into packets

packet-switching characteristic:  
store and forward:entire packet must arrive at router before it canbe transmitted on next link    
transmission delay  
end-end dealy  （端到端传输时延）  
one-hop  （单跳）

Packet queuing and loss :  
packets will queue,waiting to be transmitted on output lin ( arrival rate > transmission rate )  
packets can be dropped(lost) if memory(buffer缓存区) in router fills up  

two key network-core functions :   
forwarding（转发,local action，将数据包从一个网络接口转发到另一个网络接口，forwarding是路由器执行的实际操作，将数据包从输入接口转发到合适的输出接口） and routing（路由，global action，确定数据包从援助机到目标主机的路径的过程，routing是网络中选择数据包传输路径的决策过程）

Circuit Switching（电路交换）like call guaranteed，no sharing  
Circuit Switching : FDM and TDM  
Frequency Divison Multiplexing(FDM)频分复用    
Time Division Multiplexing(TDM)时分复用  
FDM频分复用的各路信号在同样的时间占用不同的带宽资源  
TDM时分复用的所有用户在不同的时间占用相同的频带宽度  
(figure in prof's slides)  

**numerical example**（记得补充）

ISP,IXP,content provider

**loss , delay , throughput**

nodal dalay = nodal processing delay + queue delay + transmission delay + propagation delay  
节点总时延=节点处理时延+排队时延+传输时延+传播时延

计算题examples（以后补充）

Packet loss : packet arriving to full buffer is lost , may be retransmitted by previous node ,by source end system ,or not at all

Throughput（吞吐量） : rate (bits/time unit) at which bits are being sent from sender to receiver（表示单位时间内通过某个网络/信道/接口的实际数据量）  
instantaneous(瞬时吞吐量);average(平均吞吐量)

Internet protocol stack  
application  
transport  
network  
link  
physical  

ISO/OSI reference model 7layers
application  
presentation  
session  
transport  
network  
link  
physical  

**Application layer is coming soooooon~**

**Transport Layer**

Services : provide logical communication between application processes running on different hosts (在不同主机上运行的应用程序进程之间提供逻辑通信)

Transport protocols actions in end systems:  
sender: breaks application messages into segments, passes to network layer  
receiver: reassembles segments into messages, passes to application layer  
Transport Layer Actions:  
Sender : 1. is passed an application-layer message  
2. determines segment header fields values(确定分段标题字段值)  
3. creates segment  
4. passes segment to IP  


CORE two transport protocols : TCP , UDP 

network layer VS. transport layer  
network layer : logical communication between hosts  
transport layer : logical communication between processes










