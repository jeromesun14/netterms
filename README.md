# netterms
Computer Network Terms Glossary

## Coflow
* 一个详细的PPT：[coflow-talk](http://www.mosharaf.com/wp-content/uploads/coflow-talk-qual-04112013.v2.ppsx)
* 论文PDF：[Coflow: A Networking Abstraction for Cluster Applications](http://conferences.sigcomm.org/hotnets/2012/papers/hotnets12-final51.pdf)

> We propose coflow, a networking abstraction to express the communication requirements of prevalent data parallel programming paradigms. Coflows make it easier for the applications to convey their communication semantics to the network, which in turn enables the network to better optimize common communication patterns.

## data locality
数据局部性

## DCN
Data Center Networks

## Job, task and data
* job, task + data 
* task, use CPU and memory 
* data, use network and storage

## Low latency analytics

## low overhead
低开销

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

## RSA
[腾讯云 - 服务器资源池化技术趋势](http://www.cctime.com/html/2015-4-22/20154221716419323.htm)。服务器资源池化。Intel提出了RSA（Rack Scale Architecture）架构、Google携手伯克利大学提出了WSC（Warehouse Scale Computer）的概念。Intel的RSA架构已经有了清晰的架构设计和路标，目前原型机已经面世。而Google的WSC仍在概念阶段，只有简单的时间表，2020年。

Intel RSA(Rack Scale Architecture) 架构提供了一种机架重构的方案，其思想是将几种重要的资源池化：CPU 池、内存池、存储池，池化的RSA 模型可以很方便地进行管理和扩展，并降低运行维护成本。业务软件或者OS的视角看到的还是一台传统的服务器，有CPU、内存、硬盘、网卡等。

服务器重构并资源池化后，面临的最大的挑战就是：

* 挑战一：互连与时延（拓扑结构与接口）；
* 挑战二：配置与管理（协议与监控）。

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



