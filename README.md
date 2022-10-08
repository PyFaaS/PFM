# PyFaaS Model

PyFaaS 是基于 Python 语言的轻量化 Serverless FaaS 平台，核心特点是基于可插拔的模块化设计思想，可以为使用者提供高度自定义的 FaaS 平台能力。通过 PyFaaS，用户可以快速的构建私有化 Serverless FaaS 平台，并根据需求调整不同模块的工作策略，以用于轻量化私有 FaaS 平台建设或 Serverless FaaS 相关的科学研究。

PyFaaS Model 是 PyFaaS 与其生态的规范模型，用来规约 PyFaaS 和相关生态的技术结构。通过 PyFaaS Model，可以进一步了解 PyFaaS 的设计思想以及技术原理，并对 PyFaaS Module 与 PyFaaS Module 生态等，有进一步的理解。

## 项目架构

PyFaaS 项目整体由三层组成：

![](https://www.images.wiki/y3AS4vA5c769Z66iA8h1.png)

- **应用层**：客户端等相关内容，偏向如何使用 PyFaaS，包括不限于命令行工具，Web 控制台以及相对应暴露的 API & SDK 等；
- **架构层**：由 PyFaaS 系统与 PyFaaS Module 及其生态组成；
- **规范层**：PyFaaS Model（本模型规范），即 PyFaaS 与 PyFaaS 相关生态的规范与模型；

PyFaaS 核心架构如下图所示：

![](https://www.images.wiki/3u4ry2sAGE3A29xjf2yB.png)

## 项目特点

![](https://www.images.wiki/FdrSbyqslZ9Ac82xcEhx.png)

作为开源的 Serverless FaaS 平台，PyFaaS 项目的主要应用场景是构建轻量化 FaaS 平台以及进行 Serverless 相关的科学研究，项目的核心优势与价值主要是：

1. **模块自定义**：项目采用灵活的，可高度自定义的模块化思路进行构建；将核心逻辑按照功能划分为若干模块，模块之间通过 RPC 协议进行通信，进一步实现自由定义，随时插拔；
2. **多模触发**：项目触发机制分为同步触发和异步触发，可以进一步满足更多的业务场景；通过 PyFaaS 项目，用户不仅仅可以通过 Webhook 与 Github 等平台进行快速集成，还可以通过定时任务以及触发模块的自定义能力，进一步拓展触发策略；
3. **多云混合部署**：基于模块化建设思路，PyFaaS 项目可以实现多种模式的调度方案，不仅仅可以调度本地容器实例，调度远程容器实例，还可以进一步的调度云上的 FaaS 产品，包括不限于阿里云函数计算，华为云函数计算工作流等；
4. **一键快速搭建**：PyFaaS 项目采用 Docker 容器化技术进行构建，通过脚本语言的便利性，可以实现一键搭建，快速启停，灵活插拔模块等诸多能力；
5. **开源开放**：项目本身以开源形式进行开发和迭代，PyFaaS Module 和其生态则以开放形势与海量社区用户进行共建，PyFaaS 项目不仅仅是社区的，更是每一位开发者的；
6. **模块可插拔**：基于模块化的设计思路，PyFaaS Module 将会有这严格的模块声明模型以及标准的
输入输出规范，基于这套规范与 PyFaaS Module Hub，用户可以实现快速搜索模块，快速安装并生效模块，进一步提高项目的可拓展性；

## 模型规范

模型本身由 PyFaaS 项目驱动：

| 模型版本            | 包含内容                                                                                                                                  | 对应 PyFaaS 版本 | 
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [v0.0.1](./zh/0.0.1) | [PyFaaS Framework Model](./zh/0.0.1/PyFaaS Framework Model) <br/>  [PyFaaS Module Model](./zh/0.0.1/PyFaaS Module Model) <br/>  [PyFaaS Module Hub Model](./zh/0.0.1/PyFaaS Module Hub Model) | v0.0.x       |

## 社区贡献

> 有关详细信息，请参阅[贡献指南](./CONTRIBUTING.md)。

针对 spec 的贡献也可以参考以下内容：
- 将 `PyFaaS/spec` 仓库 `fork` 到自己的账号/组织下；
- 对 `spec` 内容进行修改，更新，完善；
- 提`Pull requests`到仓库`PyFaaS/spec`的`main`分支下；并添加 [`Anycodes`](https://github.com/anycodes) 等作为Reviewers，同时在Comment中填写好更新理由；


## 开源协议

PyFaaS 是一个遵循 [Apache 2.0](./LICENSE) 协议的开源项目。

PyFaaS 使用的其他第三方的依赖库都可能有其遵循的协议，我们推荐你阅读并了解这些协议，因为其中的条款可能和 Apache 2.0 协议中的不完全相同。
