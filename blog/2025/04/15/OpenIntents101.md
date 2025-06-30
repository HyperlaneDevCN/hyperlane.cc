---
title: Open Intents 框架：构建 “意图” 新范式
description: 该框架旨在实现一个简单目标：为每个人提供 Intents，与每个人合作
slug: OpenIntents101
authors:  [Marcus, HyperlaneCC]
tags: [hyperlane, 跨链桥, OpenIntents, 示例]
image: https://pbs.twimg.com/media/GkKZ-HzaAAEpS_x?format=jpg&name=medium
hide_table_of_contents: true
---

![](https://pbs.twimg.com/media/GkKZ-HzaAAEpS_x?format=jpg&name=medium) 

# Open Intents 框架：构建 “意图” 新范式

**介绍 Open Intents 框架**  
该框架旨在实现一个简单目标：为每个人提供 Intents，与每个人合作。
随着跨链意图成为以太坊未来互操作性的核心，解算器、互操作提供商和跨链构建者对即用型、协议无关功能的需求变得更加迫切。

---

## Intents 的崛起

如今的以太坊生态系统已自然形成多链格局。用户可以在 Arbitrum 上使用主流 DeFi 协议，在 Base 上体验新型去中心化社交网络，或在 Mode 上尝试 AI 智能体。索尼等科技巨头正在 OP Stack 上构建 Layer2，ZK Rollup 技术也在快速发展。以太坊成功实现了扩容，但用户在不同 Layer2 网络间转移资产的需求导致了体验的割裂与低效——这也催生了 **Intents（意图）** 的崛起。

Intents 的核心价值——以及其采用率持续攀升的原因——在于它带来的 **革命性无缝用户体验**。要让以太坊真正实现“单链化”体验，用户需要在 2 秒内完成跨链资产转移。Intents 技术赋予了这种能力：快速、无摩擦的跨链资产流转。用户只需声明意图（例如“将 Base 链上的 100 USDC 兑换为 Arbitrum 链上的 100 USDT”），专业化执行代理（即 **Solver**）便会自动完成操作。Solver 将处理所有复杂环节，包括寻找最优执行路径、完成交易结算，并承担[终局性风险](https://medium.com/across-protocol/dodging-the-finality-bullet-a-guide-to-finality-risk-7a1eef00271a#:~:text=Finality%20risk%20is%2C%20therefore%2C%20the,on%20the%20network%20(exploits).)。

然而，对于新兴链而言，集成 Intents 并非易事。开发者需要说服现有协议认可其链的价值，这往往涉及漫长的业务拓展流程。若想自主运营 Solver，则需自建基础设施并承担结算、流动性再平衡等成本。总体而言，Solver 的流动性管理和资源整合仍是重大挑战。

尽管开发者持续探索 Intents 的创新路径，但从概念到落地仍困难重重。开发者不得不独自构建完整的 Intents 技术堆栈——从智能合约、结算层、Solver 集成到用户界面，每个环节都需要亲力亲为。

以太坊生态的繁荣始终源于协作创新。如果有一种方式能在 Intents 基础设施层面实现共建共享，是否能大幅降低采用门槛，推动技术规模化？

---
<!-- truncate -->
## Open Intents 框架

Open Intents Framework 是一个模块化、开源的开发框架，致力于简化 Intents 产品的构建与部署流程。开发者无需从零搭建基础设施，而是可以基于模块化抽象组件（包括标准化 Solver、可组合智能合约等）快速定制 Intents 协议。

通过将 Intents 技术堆栈中的 **Solver 执行** 与 **交易结算** 等核心环节模块化，Open Intents Framework 赋予开发者“积木式搭建”的灵活性。开发者可根据具体需求自由组合最优解决方案，避免被单一供应商技术绑定，真正实现“以开发者需求为中心”的架构设计。

🔑 **生产就绪的 ERC-7683**

[ERC-7683](https://www.erc7683.org/) 标准统一了 Intents 的创建、执行和结算流程，以改善以太坊跨链用户体验。该标准获得了以太坊社区的广泛支持，包括 [Vitalik Buterin](https://x.com/AcrossProtocol/status/1819719966318309682) 等生态领导者。

Open Intents Framework 提供了一个开源的 [ERC-7683 参考实现](https://github.com/BootNodeDev/intents-framework/tree/main/solidity#erc7683-reference-implementation)，任何人都可以直接使用或调整。这与 Across Protocol 最近发布的 [主网 ERC-7683 合约](https://docs.across.to/use-cases/erc-7683-in-production) 相辅相成。两种实现表明，标准化 Intents 已准备好投入生产使用，并满足以太坊去中心化生态的多样化需求。

### 核心功能

Open Intents Framework 包含几个关键组件，初始实现已在 [Github 仓库](https://github.com/BootNodeDev/intents-framework) 中提供：

📖 **开源 Solver 实现** 
一款基于 TypeScript 的应用程序，设计用于监控链上事件并处理 Intents。当前大多数 Solver 依赖于为特定 Intents 系统定制的基础设施，而此 [共享参考 Solver](https://github.com/BootNodeDev/intents-framework/tree/main/typescript/solver) 提供了协议无关的功能——如索引、交易提交和再平衡——任何人都可以根据自身需求进行调整和定制。这一实现补充了 Across Protocol 已有的 [参考中继器](https://docs.across.to/relayers/running-a-relayer)，为 Solver 代码库带来了客户端多样性。

🏗️ **可组合智能合约**  

一套 [预构建智能合约](https://github.com/BootNodeDev/intents-framework/tree/main/solidity)，基于 ERC-7683 定义了 Intents 的解释、执行和结算逻辑。框架默认提供了基本限价单交换和 [Hyperlane ISM](https://docs.hyperlane.xyz/docs/protocol/ISM/modular-security) 结算实现，但其核心 [Base7683 合约](https://github.com/BootNodeDev/intents-framework/blob/main/solidity/src/Base7683.sol) 是模块化的，可支持不同订单类型和结算机制的定制。这种灵活性让开发者能够构建更快、更具表现力、更安全的 Intents。Arbitrum 的广播标准也适用于此。

🎨 **UI 模板** 
一个预构建、可定制的 UI 模板，让终端用户能够轻松使用 Intents。

### 为所有人提供 Intents，与所有人合作

Open Intents Framework 是一个公共物品倡议，由 EF、[Hyperlane](https://hyperlane.xyz/) 和 [Bootnode](https://www.bootnode.dev/) 的贡献者共同领导，目标是为整个以太坊生态带来开放、无需许可的 Intents。该项目由 Hyperlane 提供初始资金启动，为其成长为社区拥有、社区资助的公共物品奠定了基础。

通过 Open Intents Framework 提供的全面模块化开源工具套件，希望在 Intents 技术栈上创新的团队不再需要从头构建。他们可以更快地迭代并部署给真实用户，降低开销，并根据具体需求定制 Intents 协议。**为所有人提供 Intents，与所有人合作。**

因此，这为以太坊生态系统开启了新的可能性：

- 可以轻松尝试不同的订单类型，如跨链荷兰拍卖。
- 运行 Solver（尤其是在不同 Intents 协议之间）变得更加容易。
- 链可以自行部署 Intents 基础设施，无需现有 Intents 协议的许可或兴趣。
- 可以创建不同的结算机制，并随时间迁移。
- 用户可以无缝地跨链移动资产和数据。

> **开放协作以标准化 Intents，正成为统一以太坊的关键。**

标准化接口如 ERC-7683 或 [RRC-7755](https://github.com/base/RRC-7755-poc)（一种指定目标链上具体调用的标准）非常重要，但支持这些标准需要构建大量基础设施。避免重复工作可以加速 Intents 的普及。

### Intents 结算多样性

虽然框架默认提供了一个简单的 Hyperlane 结算选项，但其设计鼓励开发者构建具有替代结算机制的 Intents 协议。例如 [RRC-7755](https://github.com/base/RRC-7755-poc)，通过利用存储证明来验证目标链上的调用执行，消除了除以太坊及其 Rollup 已有信任假设之外的其他假设。[Hashi 的 Oracle Aggregator](https://crosschain-alliance.gitbook.io/hashi)、[Espresso 的确认层](https://www.espressosys.com/)、[Optimism 的 Superchain 原生互操作性](https://docs.optimism.io/superchain/superchain-explainer) 或 [Arbitrum 的跨链广播标准](https://medium.com/offchainlabs/bringing-interoperability-to-arbitrum-and-ethereum-ba97ea99d9ff) 都可以作为结算模块轻松添加到 Base7683 合约中，使 Intents 结算更快更好。以太坊基金会工作组研究的跨链消息标准，如 [ERC-7786](https://github.com/ethereum/ERCs/pull/673)（由 [OpenZeppelin](https://www.openzeppelin.com/)/[Axelar](https://www.axelar.network/) 提出）、[ERC-7841](https://github.com/ethereum/ERCs/pull/766)（由 [Espresso](https://www.espressosys.com/) 提出）或 [ERC-7854](https://github.com/ethereum/ERCs/pull/817)（由 [Hyperlane](https://hyperlane.xyz/) 提出），也能通过其模块化验证无缝结算 Intents。

### 参考 Solver

在开发即将推出的 Eco Protocol 时，Eco 团队最近发布了 [Eco Routes](https://eco.com/blog/eco-launches-routes-in-beta/)，一个链上框架，使应用和区块链能够访问无需许可的跨链稳定币流动性。作为这项工作的一部分，Eco 一直在探索如何调整 Open Intents Framework 的参考 Solver，使其成为 Eco Routes 的标准 Solver。

### Solver 的流动性管理

帮助 Solver 管理流动性将是加速 Intents 采用的关键。[Everclear](https://www.everclear.org/) 正在将模块化再平衡功能集成到参考 Solver 中，为更多 Solver 带来自动化再平衡。

此外，Arbitrum 基金会将利用 [Nomial](https://nomial.io/) 作为 Arbitrum 通用 Intents 引擎的一部分。Nomial 也计划为参考 Solver 添加一个 Nomial 模块。

### Solver Intents 匹配

当前框架实现（与大多数协议一样）依赖用户在源链上提交其 Intents，以便 Solver 完成。资源锁是一种有前景的改进方式。Uniswap 通过 [The Compact](https://github.com/Uniswap/the-compact/) 处于领先地位，并一直在合作研究如何通过 Compact 路由的 Intents 进行报价、与 Open Intents Framework Solver 沟通并完成。框架 Solver 还可以通过 [Khalani](https://khalani.network/) 等平台相互协作，扩大覆盖范围，使 Solver 功能更广泛地适用于任何区块链上的应用。

用户界面和钱包最终让用户能够创建这些 Intents。[Superbridge](https://superbridge.app/) 已探索如何轻松添加框架模块，从而降低新 Intents 协议的集成难度。

---

### 一起构建，一起胜利

ERC-7683、Arbitrum 的 [通用 Intents 引擎](https://medium.com/offchainlabs/bringing-interoperability-to-arbitrum-and-ethereum-ba97ea99d9ff) 和现在的 Open Intents Framework 揭示了一个简单的事实：**一起构建，一起胜利**。统一以太坊不是一个团队能完成的，需要整个社区。通过拥抱开放基础设施和共享工具，我们可以作为社区一起构建一个无需信任的去中心化未来。

---

## 如何参与

- 在官方 Open Intents Framework 论坛 [页面](https://github.com/BootNodeDev/intents-framework/discussions/89) 提供您的反馈和评论。
- 探索 [Github 仓库](https://github.com/BootNodeDev/intents-framework/tree/main)。
- [OpenIntents](https://www.openintents.xyz/#1976d35200d68051bfe5f0bdb3ced9bc)
