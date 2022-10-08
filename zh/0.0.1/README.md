# PyFaaS Model (PFM) v0.0.1 文档

## 基本信息

| 版本 | v0.0.1                                                       |
| ---- | ------------------------------------------------------------ |
| 作者 | 发起人：[`Anycodes`](https://github.com/anycodes)            |
| 时间 | 2021.9.16                                                    |
| 内容 | [PyFaaS Framework Model](./PyFaaS Framework Model) <br />[PyFaaS Module Model](./PyFaaS Module Model) <br />[PyFaaS Module Hub Model](./PyFaaS Module Hub Model) |

## 简介

PyFaaS Model (PFM) 是 PyFaaS 项目与相关生态的模型规范，由 PyFaaS 社区发起编写。

![](https://www.images.wiki/shydk1AZ4i39vdtrzfxt.png)

如上图所示，该模型文档主要从模型开发者以及 PyFaaS 用户等两个角色的开发流程、使用流程出发，针对 PyFaaS Module 规范，PyFaaS Module Hub 规范以及 PyFaaS 本身的一些架构设计，进行描述与规约。通过该模型文档：

1. 了解 PyFaaS 的设计初衷、工作原理；对 PyFaaS 将会有一个更为深入的认识；
2. 了解 PyFaaS 的模块化设计思路，并可以根据模型规范，进行模块的开发；
3. 了解 PyFaaS 的模块生态，对可高度自定义的轻量化 FaaS 平台 PyFaaS，将会有更为深入的了解。

### 角色规约

1. **PyFaaS 用户**（英文表达：**PyFaaS User** 或 **System Administrator**），指的是 PyFaaS 搭建者。例如，小明通过 PyFaaS 开源项目，自己搭建了私有化 FaaS 平台，那么小明就是所谓的 PyFaaS 用户；
2. **模块开发者**（英文表示：**Module Developer**），指的是模块的开发者。例如，小明发现 PyFaaS 默认的 Scaling 模块算法过于单一，在其私有化的 FaaS 平台中表现并不是非常好，所以小明根据规范，自己开发了一个 Scaling 模块，此时小明就是所谓的 PyFaaS 用户；
3. **普通用户/使用者**（英文表示：**User**），指的是外部用户。例如，小明通过 PyFaaS 开源项目，自己搭建了私有化 FaaS 平台，并在平台中创建了一个 Web 应用，此时小红等人通过互联网访问了该 Web 应用，此时小红就是所谓的普通用户或使用者；

### 模型规约

1. **PyFaaS Framework Model**：是对 PyFaaS 系统的介绍，包括设计目的，实现原理等内容；同时也包括用户在使用该系统时的一些约定，包括不限于 API 规范、通信协议等相关内容；
2. **PyFaaS Module Model**：是对 PyFaaS Module 的规约，基于 PyFaaS Module Model，开发者可以定制化开发 PyFaaS 的不同模块，以获得更为灵活和高度自定义的能力（PyFaaS Module 开发者只有根据该模型/规范进行模块的开发，才可以被 PyFaaS 所识别与加载/引用）；
3. **PyFaaS Module Hub Model**：是 PyFaaS 项目针对可插拔模块（Module）的共享平台。PyFaaS Module 开发者可以将开发完成且符合 PyFaaS Module Model 的模块发布到 PyFaaS Module Hub，以便其它 PyFaaS 平台所有者快速进行使用。

### 描述规约

1. **应**：表示“必须”的意思，可以用“必须”、“需要”等词进行代替；
2. **宜**：表示“最好要这样做”的意思；
3. **可**：表示“可以这样做”的意思；
4. **不应**：不是“不应该这样做”的意思，可以用“不可”等词进行替代；
