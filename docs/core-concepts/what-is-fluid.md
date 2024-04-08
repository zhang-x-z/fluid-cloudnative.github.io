---
sidebar_label: What is Fluid
sidebar_position: 1
slug: /
---

# What is Fluid

Fluid is an open source Kubernetes-native Distributed Dataset Orchestrator and Accelerator for data-intensive applications, such as big data and AI applications. It is hosted by the [Cloud Native Computing Foundation](https://cncf.io) (CNCF) as a sandbox project.


## Target Scenario and  Values

In the treand of computation and stroage separation, the goal of Fluid is to enable AI/Big Data Applications to use data from any storage more efficiently with a high-level abstraction manner  and without changes to the applications themselves.

Through the data abstraction layer powered by Fluid on Kubernetes, the data will just be like 
the fluid, waving across the storage sources(such as HDFS, OSS, Ceph) and the cloud native applications on Kubernetes. It can be moved, copied, evicted, transformed and managed flexibly. Besides, All the data operations are transparent to users. Users do not need to worry about the efficiency of remote data access nor the convenience of data source management. User only need to access the data abstracted from the Kubernetes native data volume, and all the left tasks and details are handled by Fluid.

Fluid aims to turn different distributed cache systems(Alluxio, JuiceFS, Vineyard,  CubeFS and so on) into self-managing, self-scaling, self-healing and observable cache services inside of Kubernetes by providing the common framework of Fluid.

Fluid enables Kubernetes schedulers to make intelligent, topology-aware scheduling plans regarding where the distributed data cache system is located.  It focuses on the dataset orchestration and application orchestration  scenarios. The dataset orchestration can arrange the cached dataset to the specific Kubernetes node, while the application orchestration can arrange the the applications to nodes with the pre-loaded datasets. These two can work together to form the co-orchestration scenario, which take both the dataset specifications and application characteristics into consideration during resouce scheduling.

Fluid presents its value in the following two aspects:
1. Use the power of Kubernetes platform to deliver its services via a Kubernetes Operator for each distributed cache provider, and automate the tasks of the administrator: deployment, bootstrapping, configuration, provisioning, scaling, upgrading, monitoring, data prefetch, data migration and resource management.
2. Help the users make the most of distributed caching by combining third-party caching systems with Kubernetes scheduling and elasticity, also aligning them with specific application data usage scenarios and methods.

## Why Cloud Native needs Fluid

There exist a nature divergence between the cloud native environment and the earlier big data processing framework. Deeply affected by Google's GFS, MapReduce, BigTable influential papers, the open souce big data ecosystem keeps the concept of 'moving data but not moving computation' during system design. Therefore, data-intensive computing frameworks, such as Spark, Hive, MapReduce, aim to reduce data transmission, and consider more data locality architecture during the design. However, as time changes, for both consider the flexibility of the resource scalability and usage cost, compution and storage separation architecture has been widely used in the cloud native environment. Thus, the cloud native ecosystem need an component like Fluid to make up the lost data locality when the big data architecture embraces cloud native architecture.

Besides, in the cloud native environment, applications are usually deployed in the stateless micro-service style, but focus on data processing. However, the data-intensive frameworks and applications always focus on data abstraction, and schedules and executes the computing jobs and tasks. When data-intensive frameworks are deployed in cluod native environment, it needs component like Fluid to handle the data scheduling in cloud.

To resolve the issue that Kubernetes lacks the awareness and optimization for application data, Fluid put forward a series of innovative methods such as co-orchestration, intelligent awareness, joint-optimization, to form an efficient supporting platform for data-intensive applications in cloud native environment.

## Publication
For more information of our key ideas, please refer to our papers:

1. **Rong Gu, Kai Zhang, Zhihao Xu, et al. [Fluid: Dataset Abstraction and Elastic Acceleration for Cloud-native Deep Learning Training Jobs](https://ieeexplore.ieee.org/abstract/document/9835158). IEEE ICDE, pp. 2183-2196, May, 2022. (Conference Version)**

2. **Rong Gu, Zhihao Xu, Yang Che, et al. [High-level Data Abstraction and Elastic Data Caching for Data-intensive AI Applications on Cloud-native Platforms](https://ieeexplore.ieee.org/document/10249214). IEEE TPDS, pp. 2946-2964, Vol 34(11), 2023. (Journal Version)**