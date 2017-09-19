# Workshop on Recent Topics in High Performance Computing

Date: September 21, 2017. 1pm-5pm  
Venue: Kagaku-Kaikan, 1-5 Kanda-Surugadai, Chiyoda-ku, Tokyo 101-8307, Japan

This workshop aims to give the [HPCAsia'18](http://sighpc.ipsj.or.jp/HPCAsia2018/) program committee members an opportunity to discuss their research and to foster development of a
strong research community among Asia/Pacific regions. Every PC member
who attends the face-to-face meeting on September 22 is invited to
attend and give a short talk at this workshop. Note that giving a talk
is optional; it is still highly encouraged to join even if you do not
wish to give a talk. If you wish to give a talk, please submit the
title and abstract as instructed below.

The workshop is also open to anyone interested. 

## Talk submission

Please submit the title and abstract from the below Google form by September 15.

[Submission form](https://goo.gl/forms/UfZnnSlERccVPhk83)

We solicit talks by the PC members of HPCAsia'18. Each talk is likely
to have about 15 minutes at the workshop. Submissions are accepted on
a first-come, first-served basis without reviews. No proceedings will
be published.

## Program (Tentative)

| 1:00 - 1:15 | Introduction |
| 1:15 - 2:15 | Session 1    |
| 2:15 - 2:30 | Break        |
| 2:30 - 3:30 | Session 2    |
| 3:30 - 3:45 | Break        |
| 3:45 - 4:45 | Session 3    |

### Session 1

**Miquel Pericas (Chalmers University of Technology)**, *Collaborative HW-SW schemes for scalable resource management*

Abstract: 
 Scalable computing requires efficient and low-overhead management of parallelism and communication. To handle the diversity of modern hardware platforms, management schemes need to be dynamic and adaptive.  A common approach is to interface the hardware and software via a runtime system that takes care of task scheduling and mapping. However, current applications and platforms do not exchange enough information to optimize parallelism and communication.
 To address this problem we are working on collaborative software and hardware solutions.  At the software level, we have developed the XiTAO runtime system that generalizes the concept of task in two ways: first, it adds resource usage annotations, and second, it provides task moldability. Generalized tasks are in shape similar to nested parallel computations. The XiTAO runtime abstracts the hardware into elastic resources partitions called elastic places, onto which the generalized tasks are executed.  At the hardware level, we are researching adaptive cache hierarchies that reconfigure themselves to match the resources required by the running applications.
 In this talk I will cover the XiTAO runtime, our research into adaptive cache hierarchies, and current research to use the XiTAO runtime as a dynamic manager for statically scheduled parallel computations within a single application.

**Marc Baboulin	(University of Paris-Sud)**, *Using randomization in sparse linear systems*

Abstract: Random Butterfly Transformations (RBT) have been successfully applied to accelerate the solution of dense linear systems by preventing the communication overhead due to pivoting. In this talk, we present experiments on direct sparse factorizations where RBT is applied with the SuperLU sparse direct solver. In particular we explain how RBT can be combined with sparsity-preserving strategies. Then we propose to integrate RBT in the iterative solver pARMS to solve more efficiently the last Schur complement system in the application of the recursive multilevel process, resulting in an improvement of convergence and accuracy.

**Naoya Maruyama (LLNL)**, *High Performance, High Productivity Programming through Domain Specialization*

Abstract: This talk will present an overview of some of our past research for achieving high performance and high productivity at heterogeneous large-scale systems. It is generally considered that performance and productivity are conflicting trade-off in HPC applications, especially when using accelerators such as GPUs. To address this challenge, we have been working on domain-specific programming frameworks that significantly ease the problem of achieving both performance and productivity. In this talk, we will show that by designing frameworks customized for specific computation patterns it is possible to automate most of the manual programming burden for parallelization and optimization.

### Session 2

**Hiroshi Inoue	(IBM Research - Tokyo)**, *Bring Apache Spark Closer to Accelerators*

Abstract: Apache Spark has been gaining popularity for processing a large amount of data on distributed clusters. To accelerate analytics and machine learning tasks for such big dataset running on Spark, we like to exploit hardware accelerators, such as GPU and SIMD instructions. Since Spark is implemented with Scala and running on Java virtual machines, which deeply virtualize underlying hardware, it is challenging to accelerate Spark applications running on JVM using accelerators. In this talk, we discuss how we conduct end-to-end software stack optimization by enhancing both Spark runtime and Java just-in-time compiler.

**IHsin Chung (IBM Research)**, *Towards a Composable Computer System*

Abstract: The recent advancement of technology in both software and hardware enables us to revisit the concept of the composable architecture in the system design. The composable system design provides flexibility to serve a variety of workloads. The system offers a dynamic co-design platform that allows experiments and measurements in a controlled environment. The goal is to speed up the system design and software evolution by adopting available technology with the understanding of application characteristics. I will discuss the experience we learned from the prototype system cluster we built.

**Hideyuki Kawashima (University of Tsukuba)**, *Accelerating Read Atomic Multi-partition Transaction with Remote Direct Memory Access*

Abstract: Many applications these days require data processing that is both efficient and reliable. Distributed databases are one way to meet these requirements, but must be updated using distributed transactions. To manage foreign key constraints, secondary indices, and materialized views in distributed environments, read atomic multi-partition (RAMP) transactions demonstrate high efficiency. RAMP transactions achieved high performance distributed transaction processing by relaxing the isolation level. However, the use of fast interconnect to accelerate performance has not yet been considered. This paper proposes the acceleration of RAMP transactions by exploiting remote
direct memory access (RDMA) on the InfiniBand interconnect. We first present GET+ and PUT+ operations that accelerate the RAMP transaction by exploiting RDMA write operations. We then present the GET* operation, which further accelerates GET+ operations exploiting RDMA read operations. To evaluate
the proposed methods, we implemented a prototype distributed in-memory key-value store in C/C++. The results of the experiments show that compared with RAMP transactions on IP over InfiniBand, GET* and PUT+ achieve a 2.67x performance improvement on the Yahoo! Cloud Serving Benchmark.

### Session 3

**Osamu Tatebe	(University of Tsukuba)**, *Gfarm/BB: Gfarm file system for burst buffers*

Abstract: Burst buffer gradually prevails in high-end super computers to fill a gap among CPU performance and I/O performance.  This talk introduces the design and implementation of Gfarm/BB that is a temporal distributed file system for node-local burst buffers.

**Takatsugu Ono (Kyushu University)**, *Developing an Interconnection Network Simulator for Energy Efficient Large Scale Networks*

Abstract: Reducing the power consumption of the interconnection network in the HPC system is an important issue. As a method of reducing the power consumption of the interconnection network, there is a method of transitioning to the low power mode during the period when the packet is not processed. In this talk, we present Trace RP, which is an interconnection simulator supporting low power mode.

**Takeshi Iwashita (Hokkaido University)**, *Algebraic Subspace Correction Method for a Series of Linear Systems*

Abstract: In this talk, an algebraic subspace correction method is introduced. The method focuses on solving a series of linear systems with an identical or similar coefficient matrix. The linear systems are sequentially processed due to the right hand side vector depending on the solution vector of the prior linear system. For the problem, we investigate the subspace correction method and its implicit version which accelerate the convergence of an iterative solver. The key to the correction method is how effective mapping operators are constructed. When the range of the mapping operator includes slow convergent error vectors, the correction method works well. We have developed a new mapping operator construction method for the problem above in which the information obtained in the prior solution steps is used. The subspace including slow convergent vectors is automatically identified. Numerical tests on electromagnetic field analyses confirm that the correction method with the generated mapping operator can accelerate the convergence of the iterative solver.

## Registration

No registration is required. Attending this workshop is for free. 

## Contact

- [Osamu Tatebe](http://www.hpcs.cs.tsukuba.ac.jp/~tatebe/)
- [Naoya Maruyama](https://people.llnl.gov/maruyama3)


  
  
