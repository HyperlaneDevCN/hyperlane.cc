---
title: TaoFi：通过 Hyperlane 解锁 Bittensor
description: TaoFi：通过 Hyperlane 解锁 Bittensor
slug:  taofi
authors:  [paultimofeev, HyperlaneCC]
tags: [TaoFi, Hyperlane, 跨链桥]
image: https://cdn.prod.website-files.com/669871c478050139b74c8e08/6835d0a2b25494bcc4267d66_taofi.jpg
hide_table_of_contents: true
---

# TaoFi：通过 Hyperlane 解锁 Bittensor

![img](https://cdn.prod.website-files.com/669871c478050139b74c8e08/6835d0a2b25494bcc4267d66_taofi.jpg)

如果只需一次简单的交换，你就能触及去中心化 AI 的未来，会怎样？

TaoFi 是一个由 Hyperlane 驱动的创新项目，旨在通过让用户从他们喜欢的区块链和钱包购买 alpha 代币，扩大对 Bittensor 生态系统的访问。

TaoFi 结合了 Hyperlane 的 **Warp Route** 和 **Interchain Account** 框架，以及 Sturdy 的 Subnet 10 优化，推出了一种全新的用户体验——通过一次交换即可访问 Bittensor。

**TaoFi 的第一阶段现已上线：**
<!-- truncate -->
- 从 Ethereum 和 Base 桥接 USDC ⏩ [https://www.taofi.com/bridge](https://www.taofi.com/bridge)
- 在 Bittensor EVM 上将 USDC 交换为 TAO ⏩ [https://www.taofi.com/swap](https://www.taofi.com/swap)
- 为 USDC TAO 池提供流动性 ⏩ [https://www.taofi.com/pool](https://www.taofi.com/pool)
继续阅读，了解 TaoFi 诞生的原因、它所构建的新用户体验，以及 Hyperlane 如何为其提供支持 ⏬

## 了解 Bittensor 和 Alpha 代币

Bittensor 是一个去中心化的 AI 平台，通过由 **Subnets**（子网）组成的网络运行。每个 Subnet 专注于特定的 AI 任务，例如[推理](https://research.ibm.com/blog/AI-inference-explained)或[训练](https://www.oracle.com/artificial-intelligence/ai-model-training/)。**矿工**（Miners）竞争执行这些任务，而 **验证者**（Validators）则评估他们的表现并以 **TAO**（Bittensor 的原生货币）进行奖励。

Subnets 会发行自己的原生代币，称为 [alpha 代币](https://docs.bittensor.com/subnets/understanding-subnets#:~:text=TERMINOLOGY%3A%20ALPHA%20TOKENS)。这些代币决定了该 Subnet 能获得多少 TAO。alpha 代币的需求越大，该 Subnet 获得的 TAO 就越多。

**然而，目前购买 alpha 代币是一个耗时且多步骤的过程：** 用户需要先下载 Bittensor 钱包，在交易所购买 TAO，然后找到他们想支持的验证者和 Subnet。

如果整个流程可以简化为一次交换，会怎样？

这就是 TaoFi 的用武之地。

## 单次交换访问 Bittensor

TaoFi 引入了一种全新的方式——通过单次交换访问 Bittensor，让用户更轻松地加入构建去中心化 AI 未来的网络。

这个想法很简单：从你喜欢的钱包或区块链上，通过一次交换购买原生 alpha 代币。

通过 TaoFi，用户将能够在 Base、Ethereum 和 Solana 上用资产交换 Bittensor 上的原生 alpha 代币。所有交换都将通过 TAO 进行，但桥接和交换过程将在后台自动处理，用户始终保留对其资产的控制权。

这为所有人带来了更好的体验：

- **用户**：可以使用熟悉的资产（如 USDC、ETH、SOL），通过熟悉的钱包（如 Phantom 或 Metamask）访问不断扩展的 Bittensor 生态系统，无需设置新钱包或在交易所购买 TAO 即可开始。
- **Subnets**：获得更深的流动性和更高的可见性，因为 TaoFi 使来自其他链和生态系统的流量更容易进入。

听起来很棒——但这一切是如何实现的呢？

## 由 Hyperlane 驱动

为了实现流畅的单次交换体验，TaoFi 依赖于几个关键的基础设施组件。虽然 Sturdy SN10 在后台处理交换路由，但 Hyperlane 的互操作性框架为从不同链访问 Bittensor 提供了支持。

Hyperlane 的框架是开源、无需许可且灵活的，非常适合为像 TaoFi 这样的独特跨链应用提供服务：

- [**Warp Routes**](https://docs.hyperlane.xyz/docs/protocol/warp-routes/warp-routes-overview)：Hyperlane 的代币桥接框架，将促进 Ethereum、Base 和 Bittensor EVM 之间的资产桥接。这些 Warp Routes 是将流动性引入 Bittensor 生态系统的基础，这些流动性将被交换为 TAO，然后再交换为原生 alpha 代币。
- [**Interchain Accounts**](https://docs.hyperlane.xyz/docs/reference/applications/interchain-account)（跨链账户，简称 ICAs）：Hyperlane 的一项独特创新，允许一条链上的智能合约调用另一条链上的合约。对于 TaoFi，这意味着用户可以从 Solana 或 Ethereum 等链上直接执行 Bittensor EVM 上的交易。

除了基础设施和工具，Hyperlane 还使 TaoFi 能够将覆盖范围扩展到新的链和虚拟机（VM）。目前，Hyperlane 已连接超过 150 条链，覆盖 5 个 VM。凭借其灵活性和无需许可的特性，TaoFi 可以轻松将 alpha 代币的访问扩展到更多新链和资产。

## 展望未来

TaoFi 背后的愿景很简单：通过提升易用性，帮助 Bittensor 生态系统成长。

TaoFi 将分多个阶段推出。目前，用户可以：

- 从 Ethereum 和 Base 桥接 USDC 到 Bittensor EVM ⏩ [https://www.taofi.com/bridge](https://www.taofi.com/bridge)
- 在 Bittensor EVM 上将 USDC 交换为 TAO ⏩ [https://www.taofi.com/swap](https://www.taofi.com/swap)
- 为 USDC  TAO 池提供流动性 ⏩ [https://www.taofi.com/pool](https://www.taofi.com/pool)

很快，用户将能够在他们喜欢的链上，用他们喜欢的资产购买原生 alpha 代币——无论是 Ethereum 上的 ETH、Solana 上的 SOL，还是更多其他选择。

敬请关注后续公告。