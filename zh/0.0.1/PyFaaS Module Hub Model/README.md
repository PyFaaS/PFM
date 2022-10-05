# PyFaaS Module Hub 模型

PyFaaS Module Hub 是 PyFaaS 项目针对可插拔模块（Module）的共享平台。PyFaaS Module 开发者可以将开发完成且符合 PyFaaS Module Model 的模块发布到 PyFaaS Module Hub，以便其它 PyFaaS 平台所有者快速进行使用。例如：

- Module 开发者针对弹性伸缩模块（Scaling Module）开发了一个基于人工智能的弹性伸缩模块，并将该 Module 发布到 PyFaaS Module
  Hub；此时通过 PyFaaS 项目构建私有化 FaaS 平台的用户，就可以快速替换自己的 Scaling Module 为该模块，以获得更高效的弹性伸缩能力；
- Module 开发者针对执行模块（Work Module）开发了一个调度到阿里云函数计算（FC）的执行模块，并将该 Module 发布到 PyFaaS Module
  Hub；此时通过 PyFaaS 项目构建私有化 FaaS 平台的用户，就可以快速将该模块增加到自己的 Work Module，以获得多云调度的能力；

PyFaaS Module Hub 模型（全称 PyFaaS Module Hub Model），是对 PyFaaS Module Hub 的规约，基于 PyFaaS Module Hub Model，任何人都可以实现私有化的 PyFaaS Module Hub。

- [目的和目标](./1.purpose_and_goals.md)
- [概述和术语](./2.overview_and_terminology.md)
- [模型规范](./3.hub_model.md)
- [适用范围](./4.application_scopes.md)
- [设计原则](./5.design_principles.md)