---
title: 无许可的互操作性
description: hyperlane
slug:  taofi
authors:  [paultimofeev, HyperlaneCC]
tags: [Hyperlane, 跨链桥]
image: https://cdn.prod.website-files.com/669871c478050139b74c8e08/67dba2488f83e96ec3783ef3_1_kBFYvpVDmHeTWtB0dLsx4g.webp
hide_table_of_contents: true
---

当前跨链互操作性领域的看门人现象是不可持续的。

- 不受支持的链上的开发者不得不恳求桥接或互操作性平台在他们的链上部署。
- 互操作性团队无法跟上所有新链的步伐，导致新链部署出现瓶颈。
- 资产发行者需要团队将他们的资产列入白名单，才能将资产转移到其他链上。

随着链和资产数量的持续增长，这种情况对双方来说都令人沮丧且难以维持。Hyperlane 提供了一个解决方案。

## 引入无许可的互操作性

无许可的互操作性意味着任何时候都可以自由地将一整套互操作性功能带到任何区块链、任何应用链或任何 Rollup 上。无需请求 Hyperlane 团队或其他任何人的许可，没有人能阻止你。通过 Hyperlane，你可以掌控自己的命运。

这一目标是加速新链的采用，释放更多流动性，并消除当前互操作性中存在的看门人障碍。受到 Cosmos [IBC 协议](https://ibcprotocol.org/documentation/) 设计的启发，无许可互操作性的愿景是将互操作性的优势扩展到不断扩大的链宇宙中。

## 简易类比

- 想象每个区块链、Rollup 和应用链是一个星球，而桥接或互操作性团队则是星际高速公路的规划者。
- 星球之间需要通过星际高速公路连接，才能实现互动或交易。
- 当前的高速公路规划者集中规划星际高速公路，团队决定哪些星球可以连接，并且一次只能专注于少数几个，这严重限制了未连接星球的增长，并将权力集中在这些团队手中。
- 如果任何人都能无需请求规划者许可，就将自己的星球或链连接到星际高速公路，参与并受益于互联星球网络的经济交换会怎样？
- 这就是 Hyperlane 提供的无许可互操作性。你不再需要依赖团队为你带来互操作性，Hyperlane 正在开放跨链高速公路。

## 无许可的 Hyperlane 功能

Hyperlane 的无许可和模块化设计支持了许多独特功能：

- [无许可部署](https://docs.hyperlane.xyz/docs/deploy-hyperlane)：将 Hyperlane 互操作性堆栈带到任何 EVM 链上，无需依赖 Hyperlane 团队（非 EVM 链的支持正在开发中）。
- **模块化安全**：完全掌控并定制你的应用程序安全模型。混合、匹配并堆叠[跨链安全模块](https://docs.hyperlane.xyz/docs/protocol/sovereign-consensus#interchain-security-modules) (ISMs)，设置参数以过滤有害交易，甚至可以构建自己的安全模块。
- [Warp Routes](https://docs.hyperlane.xyz/docs/protocol/warp-routes)：将任何资产打包并无许可地转移到任何[Hyperlane 支持的链](https://docs.hyperlane.xyz/docs/resources/addresses)上。每种资产在独立合约中隔离，并通过 ISM 提供可定制的安全措施。

此外，我们还在开发更多酷炫功能。

## 开箱即用的互操作性

- 开箱即用的 Rollup 和应用链领域正在迅速扩展，例如 Cosmos 应用链、Celestia Rollup、Polygon Supernet、Avalanche Subnet、Optimism Opchain、Arbitrum Rollup、Starknet L3、Eclipse Rollup 等。
- 这些新链数量众多，Hyperlane 团队不可能逐一部署。通过无许可部署，这些新链可以自主连接到 Hyperlane 网络。
- 更令人兴奋的是，Hyperlane 的[无许可部署](https://docs.hyperlane.xyz/docs/deploy-hyperlane)正在演变为一个开箱即用的互操作性堆栈，让你在第一天就能启动新的应用链或 Rollup，并同时具备 Hyperlane 的互操作性和桥接功能。
- 这是一种共生关系，新连接 Hyperlane 的链可以在第一天就向现有跨链应用开放。例如，新一代跨链稳定币可以让新链在创世块时就具备导入资产的能力。
- 最棒的是什么？我们与 [Celestia](https://celestia.org/) 的概念验证已在测试网上运行。如果想尝试并启动自己的开箱即用 Rollup 和互操作性堆栈，可以从[这里](https://docs.hyperlane.xyz/docs/build-with-hyperlane/celestia-+-hyperlane)开始。

## 安全探索跨链

- 安全性始终是我们的首要任务。在无许可互操作性中，问题不在于向新链发送价值，而在于从新链取回价值。风险是有限的，因为你需要其他链上应用的批准才能向它们发送消息。
- **主权共识**通过赋予应用使用不同跨链安全模块 (ISMs) 定制安全性的能力，将风险隔离在 Hyperlane 网络中。默认 ISM 允许任何新链安全接收来自成熟链的通信。
- 你可以自定义安全参数，轻松阻止新网络（你能控制与哪些链通信）向你的应用发送消息，因此即使有问题链（rug chains）接入网络，风险也很小。
- 即使恶意链接入并发送威胁性交易，你也可以通过设置逻辑过滤掉这些交易。例如，可以设定条件，限制转移流动性池 10% 以上的消息。

## 终局愿景

我们设想了一个终局场景：在部署区块链时，你可以从一个菜单开始，只需几次点击就能定制并启动你的整个 Hyperlane 互操作性堆栈。选择所需的安全模块、要过滤的消息参数、支持桥接的资产、初始验证者和中继者提供商，以及启动时要连接的链。随时随地实现互操作性，所有功能集成在一个界面中。

这就是 Hyperlane。