# RR IJRR Revision Decomposation

参考两个已发表数据集网页，比较稳定的共同特征是三点：

1. **首页能立刻说明数据集是什么、能做什么**；

2. **网站与 devkit 是紧密绑定的**，不是分离的两个孤岛；

3. **读者能顺着网站一路走到 Getting Started、Data、Examples、Benchmark/Devkit**。

MILUV 的网页就很典型：顶部导航直接包含 Home、Getting Started、Data、Examples，首页同时概述数据内容和 devkit 内容，还把仓库结构直接展示出来。([decargroup.github.io](https://decargroup.github.io/miluv/ "Home | MILUV"))  
Boreas 的公开页面结构则强调了 **Documentation / Paper / Devkit / Leaderboard / Submission / Download** 这些关键入口，论文与配套开发包、下载和 benchmark 入口是成体系组织的。([boreas.utias.utoronto.ca](https://www.boreas.utias.utoronto.ca/?utm_source=chatgpt.com "The Boreas Dataset"))

---

## 振宇：项目网页 to-do list

### 一、Necessary Items

这些是 **不做就不建议 resubmit** 的内容。

| 优先级 | 任务                     | 具体要求                                                                                                    | 标准                             |
| --- | ---------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------ |
| P0  | 搭建项目主页                 | 建立可公开访问的网址，最好是 GitHub Pages / 学校服务器 / 独立域名中的任一方案                                                        | 链接可在无登录状态下访问                   |
| P0  | 首页 Hero 区块             | 页面打开后第一屏必须包含：数据集名称、1 句定位、1 段简介、代表图、论文链接、数据链接、代码链接                                                       | 外部读者 10 秒内知道 “这是什么、去哪下载、去哪看代码” |
| P0  | 导航栏设计                  | 至少包含：Home、Getting Started、Dataset/Data、Devkit、Benchmark/Challenge、Download、Citation                     | 顶部导航点击都可达，不出现空白占位页             |
| P0  | 下载入口页                  | 明确说明数据下载方式、数据组成、版本号、许可协议、存储位置或申请方式                                                                      | huggingface入口                  |
| P0  | Devkit 页面              | 单独页面介绍 devkit 提供什么、支持哪些功能、如何安装、如何跑最小示例                                                                  | 页面能直接引导到 GitHub README 和快速开始   |
| P0  | Benchmark/Challenge 页面 | 明确任务定义、输入输出、评测指标、baseline、提交方式（若有）                                                                      | 读者能理解 benchmark 的玩法和用途         |
| P0  | Citation 页面            | RoCo Challenge @ AAAI 2026网页；RoCo Challenge @ IROS 2026 (**Accepted** Competition Proposal) Coming Soon | 可直接跳转网页                        |
| P0  | 联系方式                   | 提供维护邮箱或项目联系邮箱 rocochallenge@gmail.com                                                                   | 编辑和读者能知道如何联系项目组                |

---

### 二、首页必须呈现的具体模块

不要只做一个“宣传页”，要做成 **投稿可用的资源门户**。

#### 1. 顶部首屏

必须有：

- 数据集全名

- 一句副标题，直接说明定位

- 三个主按钮：
  
  - Paper (暂无)
  
  - Download
  
  - Devkit / GitHub

- 一张最能代表任务的图 
  最好是双臂装配场景图 + 数据模态拼图

#### 2. Dataset Overview

这一块回答：

- 任务是什么

- 为什么难

- 数据来自哪里

- simulation 和 real-world 各包含什么

- 为何对 community 有用

建议用 4–6 个 bullet，而不是一大段话。

#### 3. What’s Included

建议做成卡片式模块，至少包括：

- Real-world subset

- Simulation subset

- Annotations / task phases

- Recovery / failure cases

- Baselines

- Devkit

#### 4. Quick Start

首页就要给一个最短路径：

- Step 1: download data

- Step 2: install devkit

- Step 3: load one sample sequence

- Step 4: run one benchmark example

这一点非常重要。MILUV 的网页把 Getting Started 和 Examples 直接做成主导航，本质上就是在降低首次使用门槛。([decargroup.github.io](https://decargroup.github.io/miluv/ "Home | MILUV"))

---

## 三、页面结构建议

这是最适合执行的站点地图。

### 1. Home

内容：

- 项目概览

- 数据集亮点

- 模态/平台/任务简介

- 快速入口

- 新闻与版本更新 (可以加上我们AAAI 2026和IROS 2026的比赛新闻)

### 2. Getting Started

内容：

- 环境要求

- 安装步骤

- 数据下载

- 目录结构

- 第一个运行示例

### 3. Dataset / Data

内容：

- 数据采集平台

- 数据模态

- 文件组织方式

- 标注说明

- real vs sim 差异说明

### 4. Devkit

内容：

- devkit 目标

- 功能清单

- 安装方式

- API 入口

- data loader

- evaluation scripts

- visualization

- examples

### 5. Benchmark / Challenge

内容：

- benchmark 任务

- 指标

- baseline

- 结果解释

- challenge 与 dataset 的关系

### 6. Download

内容：

- 下载链接

- 数据版本

- checksum（最好有）

- license

- 使用协议

- 硬件/存储需求

### 7. Citation

内容：

- BibTeX

- 论文链接

- 项目链接

### 8. FAQ

内容建议：

- 数据是否公开商用

- 如何申请额外数据或自己生成仿真中的新数据

- benchmark 如何提交

- devkit 支持哪些 Python 版本，isaacsim 5.0+的话只支持Python 3.11

- 遇到 bug 去哪里提 issue？GitHub Issue区链接

---

## 四、振宇 与子恒 的协同接口

这是最关键的部分。编辑已经明确要求网页中要有 **helper functions/code / devkit / benchmark scripts**，所以网页负责人不能等代码全做完才接。网页和 devkit 要同步推进。编辑意见要求数据、helper code、benchmark usage 形成明确入口，这与参考案例是一致的。([boreas.utias.utoronto.ca](https://www.boreas.utias.utoronto.ca/?utm_source=chatgpt.com "The Boreas Dataset"))

### 振宇需要向子恒索取的内容清单

下面这些固定产物：

| 向子恒 索取         | 用途                              |     |
| -------------- | ------------------------------- | --- |
| GitHub 仓库链接    | 网页主入口                           |     |
| README 初稿      | Getting Started / Devkit 页面内容来源 |     |
| 安装命令           | 直接放到网页快速开始                      |     |
| 最小运行示例         | 首页 Quick Start 和 Examples 页面展示  |     |
| 数据目录结构         | Data 页面说明                       |     |
| benchmark 运行命令 | Benchmark 页面说明                  |     |
| 支持的功能列表        | Devkit 页面功能表格                   |     |
| 已知限制 / TODO    | FAQ 页面和说明页面                     |     |

## 五、推荐网页文案模板

下面这些句子，可以直接按结构改写。

### 首页一句话定位

“RoCo is a real-world and simulation dataset and benchmark for robotic collaborative assembly in industrial scenarios.”

### Devkit 简介

“The RoCo devkit provides data loading, parsing, visualization, and benchmark evaluation tools to facilitate reproducible use of the dataset.”

### Benchmark 简介

“The benchmark is designed to evaluate algorithmic performance on long-horizon, high-precision collaborative assembly tasks, with a particular focus on robustness, recovery, and real-world transfer.”

### Download 简介

“This page provides dataset access instructions, version information, licensing terms, and the expected directory structure for using the RoCo devkit.”

---

## 六、最简验收标准

最后只看这 6 条：

1. 打开首页，10 秒内知道这是什么项目。

2. 30 秒内找到论文、数据、代码。

3. 2 分钟内找到安装方式和最小示例。

4. 能清楚看到 devkit 提供了什么功能。

5. 能清楚看到 benchmark 是什么、怎么评测。

6. 网站内容与论文表述一致。

如果这 6 条都满足，这个工作就已经达到重投需要的实用标准了。
