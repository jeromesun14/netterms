# netterms
Computer Network Terms Glossary

## bisection bandwidth
[H3C 解释](http://www.h3c.com.cn/Solution/Data_Center_Solutions/Base_Network/How_Do_I_Do_It/White_Paper/201106/717013_30004_0.htm)：
> 对分带宽（bisection bandwidth）”是考量具有逐级收敛特征的网络拓扑的带宽利用率的单位。这个概念可简单的理解为：“将网络中的主机分成同样大小的两组，且主机都使用相同的网络链路进行互联，“对分带宽”就是这两组主机之间通信的总链路带宽。

[en.wikipedia](https://en.wikipedia.org/wiki/Bisection_bandwidth)：
> In computer networking, if a network is segmented into two equal parts, this is the bandwidth between the two parts.[1] Typically, this refers to the worst-case segmentation, but being of equal parts is critical to the definition, as it refers to an actual bisection of the network.

## Coflow
分布式任务中，在不同分布式 endpoint，存在多条并行 flow 的集合，每条 flow 都是独立的。整个并行任务的完成时间取决于最后一条流的完成时间。因此，称这个并行 flow 集为 **`Coflow`**。

* 一个详细的PPT：[coflow-talk](http://www.mosharaf.com/wp-content/uploads/coflow-talk-qual-04112013.v2.ppsx)
* 论文PDF：[Coflow: A Networking Abstraction for Cluster Applications](http://conferences.sigcomm.org/hotnets/2012/papers/hotnets12-final51.pdf)

> We propose coflow, a networking abstraction to express the communication requirements of prevalent data parallel programming paradigms. Coflows make it easier for the applications to convey their communication semantics to the network, which in turn enables the network to better optimize common communication patterns.

## CPE 

From [zh.wikipedia](https://zh.wikipedia.org/wiki/CPE)
> CPE（英文全称：Customer-premises equipment）用户驻地设备，位于用户端的网络终端设备，用于与电信运营商对接服务。CPE包括：用户自己的服务器，主机，以及LAN设备（路由器，交换机，防火墙等）以及ISP负责安装的WAN设备（CSU/DSUs，调制解调器）。CPE可以将4G信号转换为WiFi信号。2015年第二季度，全球CPE市场收入约29亿美元。


## data locality
数据局部性

## DCN
Data Center Networks

## East-west traffic （东西流量）
数据中心流量的一种类型，Server <--> Server 的流量。
与之相对应的，South-north traffic （南北流量），Server --> Client 的流量。

疑问：数据中心之间的流量，也称为东西流量吗？

## eLTE
From [Wikipedia](https://en.wikipedia.org/wiki/Huawei_4G_eLTE):
> 4G eLTE is technology based on the LTE standard, the lower case e referring to a Huawei proprietary derivative of the LTE standard (referred to as "enhanced LTE) that is intended to provide wireless broadband data access with peak downlink levels of 50Mbit/s and 20Mbit/s uplink per site in 5 MHz 10 MHz and 15 MHz frequencies.

eLTE 基于 LTE 标准，提供宽带接入服务。将传统的蜂窝网与 Internet 融合？
也有的地方将 e 理解为“enterprise”

## Erasure code
一种数据保护（恢复）技术，目前常用于云存储。阿里将其引入TFS系统，用于降低TFS存储成本，[链接](http://csrd.aliapp.com/?p=1841)。

From [很酷的糾刪碼(erasure code)技術](https://samkuo.me/post/2015/09/python-with-erasure-code/)
> 簡單地說 ， 糾刪碼是一種演算法 ， 可以將 K 個相同大小的資料區塊 (data block)， 轉成 (K + M) 個編碼後的區塊 ， 接收者可以從這 (K + M) 個區塊中 ， 任選 K 個區塊 ， 便足以還原編碼前的 K 個資料區塊 。 也就是說 ， 它允許最多 M 個資料區塊在傳輸或讀取過程中遺失或錯誤 ！

From [en.wikipedia](https://en.wikipedia.org/wiki/Erasure_code)
> In information theory, an erasure code is a forward error correction (FEC) code for the binary erasure channel, which transforms a message of k symbols into a longer message (code word) with n symbols such that the original message can be recovered from a subset of the n symbols. The fraction r = k/n is called the code rate, the fraction k’/k, where k’ denotes the number of symbols required for recovery, is called reception efficiency.

## eSDK 
Ecosystem SDK，是华为面向行业市场合作伙伴的二次开发平台。平台统一为SI/ISV提供华为各种产品的易集成、开放的功能接口。同时，根据行业应用场景，可提供具有针对性的预集成插件，助力合作伙伴快速构建满足客户个性化需求的差异化解决方案。

## Fine-grained control

粒度的概念，意为控制的粒度。
[stackexchange 中 Hellion 对 fine-grained 含义的答复](http://english.stackexchange.com/questions/8348/what-does-fine-grained-mean)
> When used in the context of "fine-grained control", for example, it carries the connotation of "very precise": a volume knob that gives you fine-grained control means that you can set your volume to the exact level that you desire, you don't have to choose only between "too quiet" and "too loud".

From [en.wikipedia](https://en.wikipedia.org/wiki/Granularity) 关于 Granularity （粒度）的概念。

> Granularity (also called "graininess", the quality of being grainy) is the extent to which a material or system is composed of distinguishable pieces or grains. It can either refer to the extent to which a larger entity is subdivided, or the extent to which groups of smaller indistinguishable entities have joined together to become larger distinguishable entities. For example, a kilometer broken into centimeters has finer granularity than a kilometer broken into meters. In contrast, molecules of photographic emulsion may clump together to form distinct noticeable granules, reflecting coarser granularity.

## FSO
vs. RF

From [en.wikipedia](https://en.wikipedia.org/wiki/Free-space_optical_communication)
> Free-space optical communication (FSO) is an optical communication technology that uses light propagating in free space to wirelessly transmit data for telecommunications or computer networking. "Free space" means air, outer space, vacuum, or something similar. This contrasts with using solids such as optical fiber cable or an optical transmission line. The technology is useful where the physical connections are impractical due to high costs or other considerations.

## GPGPU
From [zh.wikipedia](https://zh.wikipedia.org/wiki/%E9%80%9A%E7%94%A8%E5%9B%BE%E5%BD%A2%E5%A4%84%E7%90%86%E5%99%A8)
> 通用图形处理器（英语：General-purpose computing on graphics processing units，简称GPGPU或GP²U），利用处理图形任务的图形处理器来计算原本由中央处理器处理的通用计算任务，这些通用计算常常与图形处理没有任何关系。由于现代图形处理器强大的并行处理能力和可编程流水线，令流处理器可以处理非图形数据。特别在面对单指令流多数据流（SIMD），且数据处理的运算量远大于数据调度和传输的需要时，通用图形处理器在性能上大大超越了传统的中央处理器应用程序。

## GSM-R
From [en.wikipedia](https://en.wikipedia.org/wiki/GSM-R)
> GSM-R, Global System for Mobile Communications – Railway or GSM-Railway is an international wireless communications standard for railway communication and applications.
> 
> A sub-system of European Rail Traffic Management System (ERTMS), it is used for communication between train and railway regulation control centres. The system is based on GSM and EIRENE – MORANE specifications which guarantee performance at speeds up to 500 km/h (310 mph), without any communication loss.

## ICT
From [en.wikipedia](https://en.wikipedia.org/wiki/Information_and_communications_technology)
> Information and communications technology (ICT) is an extended term for information technology (IT) which stresses the role of unified communications and the integration of telecommunications (telephone lines and wireless signals), computers as well as necessary enterprise software, middleware, storage, and audio-visual systems, which enable users to access, store, transmit, and manipulate information.

## Job, task and data
* job, task + data 
* task, use CPU and memory 
* data, use network and storage

## Low latency analytics

## low overhead
低开销

## MDM

MDM （Mobile Device Management ）是企业 IT 向移动互联网过渡的平台技术，帮助企业将 IT 管理能力从传统的 PC 延伸到移动设备甚至 移动应用APP 。 随着时间的发展， MDM 厂商逐渐扩展出 MAM （Mobile Application Management），MEM（Mobile Email Management）和 MCM （Mobile Content Management）等更多功能。 Gartner 的MDM评测报告是目前行业最为权威的衡量标准。

## Parallelism
From [concurrency-basics.pdf](http://www.cs.umd.edu/class/fall2013/cmsc433/lectures/concurrency-basics.pdf)

### Parallelism
* Data parallelism
 + The same task run on different data in parallel
* Task parallelism
 + Different tasks running on the same data
* Hybrid data/task parallelism
 + A parallel pipeline of tasks, each of which might be data parallel
* Unstructured
 + Ad hoc combination of threads with no obvious toplevel structure 

### Data Parallelism example

Example: convert all characters in an array to upper-case

* Can divide parts of the data between different tasks and perform the tasks in parallel
* Key: no dependencies between the tasks that cause their results to be ordered 


### Task Parallelism example

* Several functions on the same data: average, minimum, binary or, geometric mean
* No dependencies between the tasks, so all can run in parallel 

## PFC
Priority-based Flow Control

## RDMA
Remote Direct Memory Access.

**疑问**：RDMA 专用交换机？？

> Common RDMA implementations include the Virtual Interface Architecture, RDMA over Converged Ethernet (RoCE),[7] InfiniBand, and iWARP. [链接](https://en.wikipedia.org/wiki/Remote_direct_memory_access#Acceptance)

## RSA
[腾讯云 - 服务器资源池化技术趋势](http://www.cctime.com/html/2015-4-22/20154221716419323.htm)。服务器资源池化。Intel提出了RSA（Rack Scale Architecture）架构、Google携手伯克利大学提出了WSC（Warehouse Scale Computer）的概念。Intel的RSA架构已经有了清晰的架构设计和路标，目前原型机已经面世。而Google的WSC仍在概念阶段，只有简单的时间表，2020年。

Intel RSA(Rack Scale Architecture) 架构提供了一种机架重构的方案，其思想是将几种重要的资源池化：CPU 池、内存池、存储池，池化的RSA 模型可以很方便地进行管理和扩展，并降低运行维护成本。业务软件或者OS的视角看到的还是一台传统的服务器，有CPU、内存、硬盘、网卡等。

服务器重构并资源池化后，面临的最大的挑战就是：

* 挑战一：互连与时延（拓扑结构与接口）；
* 挑战二：配置与管理（协议与监控）。

## SD-WAN (软件定义广域网)
SDN for WAN 的理念。

> 通信服务提供商（CSPs）包括运营商、托管服务提供商和有线电视运营商，他们现在面临的挑战是怎样在商品化宽带（如高速、廉价的互联网服务）中保证服务收入和利润。软件定义广域网（SD-WAN）解决方案似乎成为了通信服务提供商为用户提高托管服务价值的一剂良药。
> 原文SDNLAB [《为什么通信服务提供商需要实现SD-WAN》](http://www.sdnlab.com/13759.html)

## South-north traffic

见`East-west traffic`

## Speculative execution

典型应用：Apache Hadoop，[Hadoop中Speculative Task调度策略](http://dongxicheng.org/mapreduce/hadoop-speculative-task)。

Speculative Task，又叫推测式任务，是指在分布式集群环境下，因为程序bug，负载不均衡或者资源分布不均，造成同一个job的多个task运行速度不一致，有的task运行速度明显慢于其他task（比如：一个job的某个task进度只有10%，而其他所有task已经运行完毕），则这些task拖慢了作业的整体执行进度，为了避免这种情况发生，Hadoop会为该task启动speculative task，让该speculative task与原始task同时运行，哪个先运行完，则使用它的结果。

Speculative Task思路是以空间换时间的，同时启动多个相同task，哪个完成的早，则采用哪个task的结果，这样明显可以提高任务计算速度，但是，这样却会占用更多的资源，在集群资源紧缺的情况下，合理的控制Speculative Task，可在多用少量资源情况下，减少大作业的计算时间。


From [wikipedia](https://en.wikipedia.org/wiki/Speculative_execution)

> Speculative execution is an optimization technique where a computer system performs some task that may not be actually needed. The main idea is to do work before it is known whether that work will be needed at all, so as to prevent a delay that would have to be incurred by doing the work after it is known whether it is needed. If it turns out the work was not needed after all, any changes made by the work are reverted and the results are ignored.
> The objective is to provide more concurrency if extra resources are available. This approach is employed in a variety of areas, including branch prediction in pipelined processors, prefetching memory and files, and optimistic concurrency control in database systems.

## Speculative Task
详见“Speculative execution”。

## State of the art

From [zh.wikipedia](https://zh.wiktionary.org/wiki/state_of_the_art)
> 最新技術。
> 在專利申請之前，使用或以任何其他方法，藉由書面或口頭敘述將每件事提供給大眾，或者在國外申請，以便具有該事物的優先權。

From [en.wikipedia](https://en.wikipedia.org/wiki/State_of_the_art)
> The term "state of the art" refers to the highest level of general development, as of a device, technique, or scientific field achieved at a particular time. It also refers to the level of development (as of a device, procedure, process, technique, or science) reached at any particular time as a result of the common methodologies employed. The term has been used since 1910, and has become both a common term in advertising and marketing, and a legally significant phrase with respect to both patent law and tort liability. In advertising, the phrase is often used to convey that a product is made with the best possible technology, but it has been noted that "the term 'state of the art' requires little proof on the part of advertisers", as it is considered mere puffery.[1] The use of the term in patent law, by contrast, "does not connote even superiority, let alone the superlative quality the ad writers would have us ascribe to the term".[2]

## TDL
Topology Description Language

## tight coupling
紧耦合

## WDM
论文[Quartz: A New Design Element for Low-Latency DCNs
Yunpeng](https://cs.uwaterloo.ca/~bernard/sigc318-liu.pdf)将 WDM + 普通交换机 用于数据中心，构成大二层网络，从根本上解决 server 到 server 的时延问题，而不是传统的增加 `bisection bandwidth`。

Google 的论文 [Scaling Optical Interconnects in Datacenter Networks Opportunities and Challenges for WDM](http://www.australianscience.com.au/research/google/36670.pdf)，描述将 WDM 用于数据中心的挑战与机遇。

以上两篇论文引入`把广域网技术用于数据中心网络的理念`。

[en.wikipedia](https://en.wikipedia.org/wiki/Wavelength-division_multiplexing)
> In fiber-optic communications, wavelength-division multiplexing (WDM) is a technology which multiplexes a number of optical carrier signals onto a single optical fiber by using different wavelengths (i.e., colors) of laser light. This technique enables bidirectional communications over one strand of fiber, as well as multiplication of capacity.




