---
title: MilkyWay 通过 Hyperlane 实现 MILK 的跨链功能
description: MILK 作为跨链代币推出，由 Hyperlane 提供支持。MilkyWay 的跨链扩展从 MILK 的桥接开始——这是它的新治理和实用代币，由 Hyperlane 作为主要桥接提供技术支持。
slug:  milkyway-takes-milk-crosschain-with-hyperlane
authors:  [paultimofeev, HyperlaneCC]
tags: [MilkyWay, 投研, 跨链桥]
image: https://cdn.prod.website-files.com/669871c478050139b74c8e08/6810f6f2068e706f8c4abc0f_milkyway.jpg
hide_table_of_contents: true
---

# MilkyWay 通过 Hyperlane 实现 MILK 的跨链功能

![图片](https://cdn.prod.website-files.com/669871c478050139b74c8e08/6810f6f2068e706f8c4abc0f_milkyway.jpg)

MILK 作为跨链代币推出，由 Hyperlane 提供支持。

MilkyWay 的跨链扩展从 MILK 的桥接开始——这是它的新治理和实用代币，由 Hyperlane 作为**主要桥接**提供技术支持。现在，用户可以通过 [Nexus](https://www.usenexus.org/?token=0x726f757465725f61707000000000000000000000000000010000000000000000&origin=milkyway&destination=bsc) 在 MilkyWay 主网和 BNB 链之间以低费用、无滑点的方式桥接 MILK。
<!-- truncate -->
MilkyWay 的这次集成还为那些希望通过加入 [Binance Alpha](https://www.binance.com/en/support/faq/detail/60cc2e54aa32453387523c10254438c1) 平台在币安上列出代币的资产发行者和团队开辟了一条新路。因为 Binance Alpha 要求代币必须存在于 BNB 链上，MilkyWay 利用 Hyperlane 的 [Cosmos SDK 模块](https://docs.hyperlane.xyz/docs/reference/alt-vm-implementations/cosmos-sdk)，将 MILK 带到 BNB 链上——无需依赖包装资产或流动性池。

桥接 MILK ⏩ [Nexus](https://www.usenexus.org/?token=0x726f757465725f61707000000000000000000000000000010000000000000000&origin=milkyway&destination=bsc)。

## **MilkyWay 是什么？**

MilkyWay 是一个为 Celestia 生态系统打造的流动性质押和再质押协议。最初，它专注于 TIA 的流动性质押，用户可以质押 TIA 来铸造 milkTIA，这是一种流动性质押代币，可以在各种 DeFi 平台上使用。

随着时间推移，MilkyWay 还推出了流动再质押服务，用户可以再质押 TIA 以及基于 TIA 的流动性质押代币（LST）来赚取更高的收益。这形成了一个活跃的共享资产池，开发者可以利用这些资产为自己的协议提供经济安全性。

### **有什么新变化？**

自从推出以来，MilkyWay 发展迅速，目前已有超过 [156k milkTIA](https://medium.com/milkyway-zone/milkyway-raises-5mn-seed-round-with-investments-from-polychain-binance-labs-and-others-80114eddde9c) 持有者，质押的 TIA 数量超过 260 万。现在，MilkyWay 通过推出 MILK——协议的新治理和实用代币——迈出了下一步。

不过，为了让 MILK 的覆盖范围和分发最大化，MilkyWay 团队意识到只在一根链上发行代币远远不够——他们需要让 MILK 实现跨链。

为了确保跨链扩展能够顺利进行，MilkyWay 需要一个互操作性解决方案，这个方案得满足以下条件：

- 覆盖多个虚拟机（VM）的广泛链支持。
- 可以根据他们的具体需求轻松定制。
- 是开源的、无需许可就能部署。

这让他们选择了 Hyperlane。

## **MilkyWay 集成 Hyperlane**

为了让 MILK 实现跨链并进入 BNB 链——一个超越 Cosmos 生态系统的链，MilkyWay 集成了 Hyperlane 的 Cosmos SDK 模块，把 Hyperlane 作为跨链扩展的**主要桥接**。通过 Hyperlane，MilkyWay 和它的用户不需要接受包装代币——MILK 现在通过 Hyperlane 的 [抵押 → 合成 Warp Route](https://docs.hyperlane.xyz/docs/protocol/warp-routes/warp-routes-overview#:~:text=Collateral → Synthetic%3A Tokens are,the destination (synthetic) chain.) 架构在 BNB 链上可用。

![图片](https://cdn.prod.website-files.com/669871c478050139b74c8e08/67f693886ef2b3c6c230652d_Hyperlane%20Cosmos%20sdk.png)

Hyperlane Cosmos SDK 模块是 Hyperlane 协议的完整实现，专为 Cosmos 链量身定制。这个模块完全开源且模块化，包含了像 MilkyWay 这样的协议实现互操作性所需的所有基本组件——**消息传递层、安全层、传输层**，以及用于代币桥接的**应用层**。[了解更多](https://hyperlane.xyz/post/hyperlane-has-arrived-to-the-cosmos-sdk)。

通过集成 Hyperlane Cosmos SDK 模块，MilkyWay 获得了：

- **多 VM 互操作性：** MilkyWay 现在可以将服务扩展到 Hyperlane 支持的 150 多个链，包括 EVM 和 SVM 链。
- **应用链主权：** MilkyWay 完全掌控自己的互操作性堆栈，可以根据具体需求定制安全模型——比如如何验证来自其他链的消息。
- **开放、无需许可的互操作性：** MilkyWay 可以按自己的条件配置和部署 Warp Routes，不需要等待 Hyperlane 的许可或批准。

MilkyWay 的这次集成是 Hyperlane Cosmos SDK 模块的首批案例之一，展示了 Cosmos 团队如何通过部署 Hyperlane 的可定制、开箱即用模块，轻松扩展到 Cosmos 之外的新链和生态系统。

## **下一步是什么？**

把 $MILK 带到 BNB 链只是 MilkyWay 跨链扩展的起点。通过将 Hyperlane 作为标准桥接集成，MilkyWay 现在可以按自己的节奏轻松扩展到新的链和生态系统——这一切都由完全开放、无需许可且可定制的互操作性堆栈驱动。更棒的是，只要使用 Hyperlane，MilkyWay 和它的用户就能获得**扩展奖励**，这些奖励会根据协议使用情况和为 Hyperlane 生成的消息活动按比例分配。[了解更多关于扩展奖励](https://medium.com/@hyperlane_fdn/what-are-expansion-rewards-934282d982ca)。

桥接 MILK ⏩ [Nexus](https://www.usenexus.org/?token=0x726f757465725f61707000000000000000000000000000010000000000000000&origin=milkyway&destination=bsc)

**想把你的代币桥接到 BSC？**

- 在 Telegram 上联系 @[CameronMichaelSmith](https://t.me/cameronmichaelsmith)。

**想开始用 Hyperlane Cosmos SDK 模块开发？**

- 深入查看[文档](https://docs.hyperlane.xyz/docs/reference/alt-vm-implementations/cosmos-sdk)，或者[联系我们](https://docs.google.com/forms/d/e/1FAIpQLSfCXkXmMiTKq_aWD1y1b65krL2rAxubfLVw1a3UXh_2wb7O4A/viewform) 获取实施帮助。

更多关于 Hyperlane Cosmos SDK 模块的链集成即将公布。

Cosmos 扩展。

## 关于 Hyperlane

作为开源的互操作性框架，Hyperlane让开发者能够：
🔗 连接任意区块链
🌉 构建自由安全通信的多链应用
所有代码完全开源，始终无需许可即可使用。
![](https://fastly.jsdelivr.net/gh/bucketio/img9@main/2025/04/24/1745474625229-cc6c5943-9168-4da4-9b59-567effd8b7a4.png)