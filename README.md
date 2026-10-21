# 🧠 skill-learn-adaptive — 个人自适应深度认知系统 (Public Edition)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill%20Ready-success)](https://claude.ai/code)

> **核心哲学**：把“等一个懂你的讲解”变成“自底向上搭建前置依赖阶梯，按需换表征直到咔哒（相变顿悟）”。

---

## 💡 为什么需要本系统？

在深学工业级中间件（如 DDS、网络协议栈、分布式系统、操作系统底层、C++ 底层机制）时，工程师与开发者最常陷入的三大深坑：
1. **概念悬空**：没有前置依赖阶梯，直接硬嚼上层协议（如一上来就背 RTPS、QoS、SeqNum），感觉轻飘飘、磕磕绊绊，穿不起完整因果链路；
2. **死记八股**：教科书堆砌无生气的抽象术语（三次握手、SYN/ACK、IP 分类），看完就忘，脑中没有物理运转的齿轮；
3. **缺乏重力**：只看懂了理想流程，但在现实世界里不知道“它坏了会死得多惨”，知识缺乏真实事故场景的抓地力。

`skill-learn-adaptive` 是专为 **Claude Code / Agent SDK** 设计的自适应认知学习技能。它通过一套持续自演进的自适应协议，将知识从“被动文字消费”重构为**“自底向上搭建阶梯 + 撬开内核打造可重玩交互机 + 极端事故场景淬炼肌肉记忆”**的深度认知闭环。

---

## 🧱 四大核心支柱

### 1. 前置依赖阶梯树（GPS 定位导航）
面对任何复杂复合型知识，先画出自底向上的物理依赖树，明确**“当前踩在哪块地基上、目标处于第几层”**。按图索骥，逐层打牢，绝不准在悬空的沙滩上硬嚼高级概念。

### 2. 物理机器内部模型（Internals）
拒绝概念口号，每次必撬开外壳看底层物理机器：
- **三列工作台**：真实系统调用代码 / 内核物理队列与网络介质 / 实时报文与硬件监控账本；
- **全动态可重玩机制**：支持「↺ 重玩本关」精准回退重放与「⟲ 清除全部进度」双击确认防误触，内置 `localStorage` 自动断点续走。

### 3. 极端事故场景锚定（Gravity Anchor）
用真实的惨烈灾难场景（如：TCP 队头阻塞导致遥控小车停顿后暴冲撞墙、纯 UDP 丢失急停命令导致无人机撞树、roscore 崩溃导致全车休克）作为检验标准，将空洞的理论直接砸实进现实重力场。

### 4. 持续变准的双记忆档案
- **`profile/PROFILE.md`**：记录学习者专属的认知触发器（什么表征让他咔哒、什么让他糊）、已验证类比库、前置阶梯原则；
- **`profile/INDEX.md`**：人-事向量表（遇事召回）、检索失败日志（拍大腿时刻）、深浅分档清单。

---

## 📂 仓库目录结构

```text
skill-learn-adaptive/
├── SKILL.md                 # 核心执行协议（Claude Code / Agent SDK 自动发现与加载）
├── README.md                # 社区使用与架构说明
├── .gitignore               # 排除操作系统及临时文件
├── profile/                 # 学习者专属记忆档案库 (开箱即用模板)
│   ├── PROFILE.md           # 学习者认知画像与类比库（随使用动态写回进化）
│   └── INDEX.md             # 案例向量索引与深浅分档清单
└── courses/                 # 16 门已交付的高保真物理交互课程网页
    ├── dds-mental-model.html                # DDS 核心中间件与 RTPS 协议
    ├── broker-vs-p2p-mental-model.html      # 集中式 Broker vs 去中心化 P2P 架构
    ├── unicast-multicast-mental-model.html  # 单播 vs 广播 vs 多播局域网物理寻人
    ├── tcp-udp-mental-model.html            # TCP vs UDP 操作系统内核机器模型
    ├── cpp-smart-pointers.html              # C++ 智能指针与拥有权生命周期
    ├── cpp-std-move.html                    # C++ 右值引用与移动语义
    ├── cpp-vtable-polymorphism.html         # C++ 虚函数表与动态绑定
    ├── linux-epoll.html                     # Linux epoll 内核红黑树与就绪链表
    ├── cmake-mental-model.html              # Modern CMake Target 属性传播模型
    ├── langchain-mental-model.html          # LangChain 1.x LCEL 管道传送带
    ├── reverse-engineering.html             # 逆向工程 PE 解剖与反汇编证据链
    ├── rea-mental-model.html                # REA 业务本体模型与 AI 因果审计
    ├── docker-mental-model.html             # Docker 镜像、容器与分层文件系统
    ├── cpp-virtual-functions.html           # C++ 虚函数与多态调用
    ├── udp-loss-prevention.html             # UDP 四种丢包死法与三条防线
    └── algorithm-complexity.html            # 算法复杂度增长率与摊还分析
```

---

## 🚀 安装与使用指南

### 1. 一键安装到 Claude Code

只需将本仓库克隆至你的 Claude Code 技能目录即可生效：

```bash
# 进入 Claude Code 个人技能目录
mkdir -p ~/.claude/skills
cd ~/.claude/skills

# 克隆本技能
git clone https://github.com/Modify6/skill-learn-adaptive-public.git skill-learn-adaptive
```

### 2. 在 Claude Code 中唤起指令

启动 Claude Code 后，即可直接调用：

```bash
# 1. 深度学习新概念（自动判断档位、画前置阶梯、打造交互机）
/skill-learn-adaptive dds中间件
/skill-learn-adaptive C++移动语义与std::move

# 2. 周末复盘（检索失败时建立人-事索引）
/skill-learn-adaptive 复盘

# 3. 遇事决策（从人-事向量库中按结构相似度召回 top-3 参考方案）
/skill-learn-adaptive 遇事 团队重构底层通信库，想砍掉自动化测试争取提早上线

# 4. 开光时刻（记录瞬间顿悟的表征与隐喻，自动沉淀至类比库）
/skill-learn-adaptive 开光 今天突然懂了多播，是靠"在项目群聊里@人然后私聊换名片"的类比
```

---

## 🌐 体验 16 套精品交互课程

仓库 `courses/` 下自带 16 套开箱即用、完全自包含（纯原生单文件 HTML+CSS+JS，无任何打包依赖）的工业级概念透视课件：

```bash
cd courses
# 使用任意静态服务器启动
python -m http.server 8899

# 在浏览器中打开即可沉浸式操作体验
http://localhost:8899/dds-mental-model.html
http://localhost:8899/tcp-udp-mental-model.html
```

---

## 📄 许可证

[MIT License](LICENSE) © 2026 Modify6
