---
title: Hyperlane × Symbiotic 推出 Restaking Vaults：跨链质押新范式
description: Hyperlane 隆重推出 Restaking Vaults！Hyperlane 现已与 Symbiotic 合作上线，为跨链 Hyperlane 消息提供经济安全性保障。
slug:  Restaking_Vault
authors:  [paultimofeev, HyperlaneCC]
tags: [Symbiotic, 投研, 跨链桥, Restaking]
image: https://fastly.jsdelivr.net/gh/bucketio/img2@main/2025/04/17/1744894164165-3a257cb7-f748-4701-a022-187fcf372b45.png
hide_table_of_contents: true
---
# Hyperlane × Symbiotic 推出 Restaking Vaults：跨链质押新范式

![img](https://cdn.prod.website-files.com/669871c478050139b74c8e08/67e1943b3d404da92f5dfec6_1_2GK-S-WHhYC6tXsv-qOj5w.webp)

Hyperlane 隆重推出 Restaking Vaults！Hyperlane 现已与 Symbiotic 合作上线，为跨链 Hyperlane 消息提供经济安全性保障。

## Hyperlane Restaking Vaults 是什么？

首批 Hyperlane Restaking Vaults 已在 Symbiotic 平台上线啦！用户存入 Vault 的资产将被用来保护跨链 Hyperlane 消息，这是 Hyperlane 迈向经济安全的第一步。

目前，来自 Renzo、Swell、MEV Capital、Gauntlet、EtherFi、P2P 和 RE7 的 ETH 和 BTC Vaults 已开放使用，不过设有比较保守的限额。未来，Hyperlane 生态会逐步引入更多 Vaults 和支持更多种类的资产。

## 它是怎么运作的？

Symbiotic 是一个无需许可的 Restaking 协议，允许用户把资产“再质押”（Restake），同时保护多个协议。这种机制既能提高质押者的资金使用效率，又能让像 Hyperlane 这样的协议更轻松地获得经济安全保障。

在 Symbiotic 上，**质押者**（Stakers）把资产存入精心挑选的 Vaults，换取代表他们仓位的流动再质押代币（LRTs）。质押者可以拿着这些 LRTs 在 DeFi 里自由使用，而他们存进去的资产则被委托用来保护 Symbiotic 上的网络，比如 Hyperlane。

通过 Symbiotic，Hyperlane 支持的每条链都会挑选一组**验证者**（Validators）。这些被选中的验证者会被加入 Hyperlane 的[默认 ISM](https://docs.hyperlane.xyz/docs/protocol/ISM/modular-security)，成为 Hyperlane 安全体系的核心部分。存入 Hyperlane Restaking Vaults 的资产会用来奖励这些验证者，而当他们成功保护跨链消息时，质押者也能拿到回报。

## 终极目标：Restaked Interoperability

Hyperlane Restaking Vaults 标志着跨链安全的一个重要里程碑：**Restaked Interoperability**（再质押互操作性）。它的核心理念是，通过再质押的资产（比如存入 Hyperlane Vaults 的那些）来为跨链消息提供经济安全保障。这种设计通过对保护跨链活动的参与者（Agents）的不当行为施加经济惩罚，大大增强了跨链安全性。
<!-- truncate -->
![img](https://cdn.prod.website-files.com/669871c478050139b74c8e08/67e19454bdf10e5210521eec_1*a11SVNL3S2A9TzhXepYCuw.png)

### 那这跟 Hyperlane 有什么关系？

Hyperlane 的[模块化安全](https://medium.com/hyperlane/building-with-modular-security-legos-1b11112ded1a)架构用了一群叫[验证者](https://docs.hyperlane.xyz/docs/protocol/agents/validators)的“助手”，专门在消息发出的源链上观察并签署消息。这一步很关键，确保目标链收到的消息真实可信。

如果某个验证者干了坏事，比如签署了源链上根本没发生的消息，那就是欺诈，会被罚款。有了 Restaked Interoperability，干坏事的验证者会直接损失钱，因为分配给他们的 Hyperlane Restaking Vaults 的质押份额会被削减甚至[*没收*](https://consensys.io/blog/understanding-slashing-in-ethereum-staking-its-importance-and-consequences)。这种机制还能进一步扩展，协议设计者会不断探索更厉害的安全架构。

有了 Restaked Interoperability，用户通过 Hyperlane 发送消息时，可以放心，因为协议有直接的经济动力来保证消息安全送达。

## 为什么选择 Symbiotic 合作？

Symbiotic 的设计跟 Hyperlane 的模块化安全架构特别搭，而且还能根据 Hyperlane 用户的需求灵活扩展。更厉害的是，Symbiotic 已经是今天[顶尖的再质押平台](https://defillama.com/protocols/restaking)。具体来说，它给像 Hyperlane 这样的开放互操作框架带来了几个大优势：

- **可定制性**：Symbiotic 的模块化架构让网络能自己调整 Vault 参数。从存取款规则到质押设置、惩罚条件，再到操作者选择，Hyperlane 的核心开发者都能按需调整。
- **灵活性**：Symbiotic 支持多种链和资产类型进行再质押，这种灵活性让它能适应不同生态。这对 Hyperlane 很重要，毕竟它现在已经覆盖了 130 多条链，还在不断扩展。
- **可扩展性**：有了 Symbiotic，Hyperlane 随时可以根据需要创建新的 Restaking Vaults，轻松扩展再质押互操作性。

## 下一步是什么？

Hyperlane Restaking Vaults 是给 Hyperlane 带来经济安全的第一步。现在，任何链或应用都能通过 Hyperlane [无需许可地连接](https://docs.hyperlane.xyz/docs/deploy-hyperlane)到其他链和虚拟机（VMs），实现快速又便宜的跨链桥接。很快，他们还能用上经济安全来保护跨链消息。

**今天就来帮忙保护扩展吧** ⏩ [Hyperlane on Symbiotic](https://app.symbiotic.fi/network/0x59cf937Ea9FA9D7398223E3aA33d92F7f5f986A2)

## 关于 Hyperlane

作为开源的互操作性框架，Hyperlane让开发者能够：
🔗 连接任意区块链
🌉 构建自由安全通信的多链应用
所有代码完全开源，始终无需许可即可使用。
![](https://fastly.jsdelivr.net/gh/bucketio/img9@main/2025/04/24/1745474625229-cc6c5943-9168-4da4-9b59-567effd8b7a4.png)