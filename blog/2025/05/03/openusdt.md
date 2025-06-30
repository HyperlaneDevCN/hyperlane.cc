---
title: OpenUSDT 来了：专为 Superchain 打造的可扩展稳定币
description: 快来了解 OpenUSDT,这是一种与 Superchain 同步扩展的统一稳定币。
slug:  openusdt
authors:  [paultimofeev, HyperlaneCC]
tags: [Openusdt, Hyperlane, 跨链桥]
image: https://cdn.prod.website-files.com/669871c478050139b74c8e08/67e196e50423a53f4a8f9905_1_yrD0uMZrMerLuF7xmmH23w.webp
hide_table_of_contents: true
---
# OpenUSDT 来了：专为 Superchain 打造的可扩展稳定币

![img](https://cdn.prod.website-files.com/669871c478050139b74c8e08/67e196e50423a53f4a8f9905_1_yrD0uMZrMerLuF7xmmH23w.webp)

快来了解 [OpenUSDT](http://openusdt.xyz/)：这是一种与 Superchain 同步扩展的统一稳定币。

OpenUSDT 由 [Celo](https://celo.org/)、[Chainlink](https://chain.link/)、[Hyperlane](https://hyperlane.xyz/) 合作开发，流动性托管在 [Velodrome](https://velodrome.finance/) 上。它是 Tether USDT 的一个可互操作版本，解决了两个关键问题：

**流动性分散。** 目前，每个没有原生 USDT 的区块链都需要部署隔离的桥接 USDT 版本。最终，每个链上都有不同版本的 USDT。

**扩展到多个链。** OP Superchain 是一个快速增长的链网络，主网上有 [30 多个链](https://www.superchain.eco/opstack)，测试网上还有几十个。稳定币如何触达所有这些新链？

## OpenUSDT 的特点
<!-- truncate -->
OpenUSDT 是一种跨链稳定币，支持：

- **互操作性**：目前可在所有主要 Superchain 网络上使用。
- **无许可扩展**：随着新 Superchain 网络的推出，可无许可地扩展到这些网络。
- **无缝过渡到原生 Superchain 互操作**：未来可无缝过渡到原生 Superchain 互操作。
- **与原生 USDT 的前向兼容性**：允许在链与链之间与 Tether 合作，逐步过渡到原生 USDT 铸造。

## 工作原理

![img](https://cdn.prod.website-files.com/669871c478050139b74c8e08/67e196d389bc4ec3e2d1bce5_1*qlIAvLLw1m219uYKuo3RQQ.png)

1. Celo 是唯一一个拥有原生铸造 USDT 的现有 Superchain 网络，因此它充当 OpenUSDT 的铸造中心。
2. Hyperlane 的 [Warp Routes](https://docs.hyperlane.xyz/docs/protocol/warp-routes/warp-routes-overview) 将 Celo 连接到其他 Superchain 网络，实现 OpenUSDT 的互操作性。
3. 在可用的情况下，Chainlink CCIP 作为 Hyperlane 的 [跨链安全模块 (ISM)](https://docs.hyperlane.xyz/docs/protocol/ISM/modular-security) 保护 OpenUSDT 转账。具体来说，CCIP 保护部署了 CCIP 的链之间以及转账价值超过 25 万美元的转账。

OpenUSDT 的许多关键功能只有通过 Hyperlane 才能实现：

- **无许可扩展**之所以可能，是因为 Hyperlane 设计为 [任何人都可以部署](https://docs.hyperlane.xyz/docs/deploy-hyperlane) 到新链上，开箱即用。
- Chainlink 安全模块和 [与未来 Superchain 原生互操作的兼容性](https://medium.com/hyperlane/introducing-superlane-superchain-interoperability-today-1d855b24b27f) 得益于 Hyperlane 的 **模块化安全** 设计。通过 [使用 ISM 进行安全定制](https://medium.com/hyperlane/modular-security-with-hyperlane-553c09411ef3)，Hyperlane 实际上是面向未来的，允许插入任何验证方法，如 Chainlink CCIP 和 Superchain 原生互操作。

## 未来展望

从今天开始，OpenUSDT 可在以下链上使用：

![img](https://cdn.prod.website-files.com/669871c478050139b74c8e08/67e196d2154b20747890e459_1*hxNTclracVOrN2tezD8qvQ.png)

Celo、Optimism、Base、Soneium、Unichain、Mode、Lisk、Fraxtal。

随着更多 Superchain 网络的推出，未来还将添加更多网络。

Velodrome 是 OpenUSDT 推出的主要交易场所。立即交易：[velodrome.finance](https://velodrome.finance/)

立即开始使用 OpenUSDT：[openusdt.xyz](http://openusdt.xyz/)

## 关于 Hyperlane

[Hyperlane](https://www.hyperlane.xyz/) 是一个开放的互操作性框架。它使开发者能够在链上任何地方连接，并构建能够在 130 多个区块链之间轻松、安全通信的应用程序。重要的是，Hyperlane 完全开源，始终无许可地构建。

[网站](http://hyperlane.xyz/) | [文档](https://docs.hyperlane.xyz/docs/intro) | [Twitter](https://twitter.com/hyperlane) | [Discord](http://discord.gg/hyperlane) | [职业](https://jobs.lever.co/Hyperlane)