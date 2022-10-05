# PyFaaS Model

![image-20221005101344959](https://www.images.wiki/y3AS4vA5c769Z66iA8h1.png)

PyFaaS 是基于 Python 语言的轻量化 Serverless FaaS 平台，核心特点是基于可插拔的模块化设计思想，可以为使用者提供高度自定义的 FaaS 平台能力。通过 PyFaaS，用户可以快速的构建自己的 Serverless FaaS 平台，并根据自己需求调整不同模块的工作策略，以用于轻量化私有 FaaS 平台建设或 Serverless FaaS 相关产品的科学研究。

PyFaaS Model 是 PyFaaS 和 PyFaaS Module Hub 的实现规范，用来规约 PyFaaS 和相关生态的技术结构

## 项目特点

![image-20221005090159732](https://www.images.wiki/FdrSbyqslZ9Ac82xcEhx.png)

PyFaaS 项目和核心优势主要包括：

1. 模块自定义：
2. 多模触发：
3. 多云混合部署：
4. 一键快速搭建：
5. 开源开放：
6. 模块可插拔：

## 架构模型

PyFaaS 核心架构如下图所示：

![image-20221005091229637](https://www.images.wiki/3u4ry2sAGE3A29xjf2yB.png)

在该架构中，主要包括几个模块：
- API Gateway：项目整体对外暴露的接入层（API 网关层，将采用 Nginx 作为核心实现方案），无论是控制流还是数据流都将会通过该模块进行接入；
- 控制模块：项目核心部分，接入模块的相关请求，在控制模块进行基本的处理。主要包括几个子模块：
  - 触发器（Trigger Plugin）：由于 PyFaaS 是 FaaS 项目，所以依旧是由事件触发为核心的项目，此处的触发器是用来接收和处理事件的部分，将与开放生态做深度融合；触发器也将会分为同步触发器和异步触发器：
    - 同步触发器：经由控制模块将会直接对执行模块进行相关操作，并等待结果返回，并将结果返回到客户端；
    - 异步触发器：经由控制模块后，直接将任务 ID 返回客户端，并将任务传递到异步模块（核心实现方案为 Kafka），经消息中间件进行排队处理后，交予执行模块执行，并将结果存储到存储模块；
  - 元信息管理（Meta Plugin）：用来管理所有基础信息，包括不限于函数基础信息（函数名、创建时间、内存分配、运行时等）、触发器信息（触发器名称、触发器类型等）等，将与存储模块进行直接交互；
  - 任务/请求（Task Plugin）：用来管理触发源、触发结果；
  - 弹性（Scaling Plugin）：根据请求等相关数据，进行弹性伸缩决策的模块；
  - 运行时（Runtime Plugin）：用来管理运行时部分；
  - 权限管理（Auth Plugin）：包括用户管理与用户权限管理；
- 存储与可观测模块：主要包括数据库与对象存储等部分以及用户采集、上报和展示相关数据指标；
- 异步模块：主要用于处理异步任务；
- 执行模块：主要包括调度以及适配两个部分：
  - 调度：如果执行模块对接了虚机或物理机等，那么执行模块要肩负起调度策略，任务下发到不同机器的方案和策略由当前模块实现；
  - 适配：所谓适配指的是当执行模块后对接了其他 FaaS 平台（例如阿里云函数计算、华为云函数计算工作流，AWS Lambda等），该模块要做好代码与对应平台的适配逻辑；













![image-20221005091246383](https://www.images.wiki/tAgiiDxtg4vc5wzlaydy.png)



![image-20221003113801914](https://www.images.wiki/k2E3sxe1bcr8A3aZFukb.png)





![](https://www.images.wiki/BqztDed3f5Ai6799FDAj.png)





![image-20221003120029537](https://www.images.wiki/klea7swbA7vD2lbBCjqs.png)



![image-20221004211445050](https://www.images.wiki/BSaCw3w9C4babbrG7CGj.png)
