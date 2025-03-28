<h1 align="center"> ERC1155-RealEstate <br></h1>
<p align="center"><strong>基于ERC1155标准的房地产NFT项目，支持跨链操作和实时房产数据获取 
<br>作者： Joe-Goldbug</br></strong>
</p>
<br>
<br>
<br>

## 📋 项目概述

ERC1155-RealEstate是一个创新性的区块链项目，旨在将现实世界的房地产资产通过ERC1155标准进行代币化。该项目利用Chainlink的去中心化预言机网络获取真实世界的房地产数据，并通过CCIP（Cross-Chain Interoperability Protocol）实现跨链资产转移，为房地产投资和交易提供了一个去中心化、透明且高效的解决方案。

### 🌟 核心价值
- **资产代币化**：将实体房地产转化为区块链上的数字资产
- **分数化所有权**：通过ERC1155标准实现房产的部分所有权，降低投资门槛
- **跨链互操作**：支持不同区块链网络间的房产NFT转移
- **实时数据集成**：通过Chainlink Functions获取真实世界的房产数据和价格
- **DeFi应用场景**：支持房产NFT的拍卖和借贷等金融应用


## 💡 核心功能

### 1. 房地产NFT铸造与管理

通过`Issuer`合约，项目可以将现实世界的房地产资产铸造为NFT。每个NFT包含以下关键信息：

- 房产地址
- 建造年份
- 土地面积
- 居住面积
- 卧室数量

这些数据通过Chainlink Functions从真实世界的房产数据API获取，确保数据的真实性和可靠性。

### 2. 跨链资产转移

`CrossChainBurnAndMintERC1155`合约实现了基于Chainlink CCIP的跨链资产转移功能：

- 在源链上锁定或销毁NFT
- 通过CCIP发送跨链消息
- 在目标链上铸造等值的NFT

这使得房产NFT可以在不同的区块链网络间自由流通，提高了资产的流动性和可访问性。

### 3. 实时房产价格数据

`RealEstatePriceDetails`合约通过Chainlink Functions获取并更新房产的价格信息：

- 挂牌价格
- 原始挂牌价格
- 税务评估价值

这些数据可用于资产估值、贷款计算和清算阈值确定，为DeFi应用提供可靠的价格基础。

### 4. 金融应用场景

项目包含两个主要的金融应用场景：

#### 英式拍卖 (EnglishAuction)

- 支持对房产NFT进行分数化拍卖
- 实现透明的竞价机制
- 自动化的拍卖结算流程

#### 房产借贷 (RwaLending)

- 以房产NFT作为抵押物进行借贷
- 基于Chainlink价格预言机的实时估值
- 自动化的清算机制保障系统安全
  
#### 租金收益分配 (RentalIncome) 

- 将房产的租金收入自动分配给NFT持有者
- 基于持有比例进行分配
- 支持多种稳定币支付
- 通过Chainlink Automation定期执行分配

#### 房产治理DAO (PropertyDAO)

- NFT持有者可对房产相关决策进行投票
- 支持装修、出租、出售等重要决策
- 投票权重与持有比例挂钩
- 提案自动执行机制

## 🔒 安全考量
- 所有合约均包含免责声明，表明这是示例代码，未经审计
- 使用OpenZeppelin的安全合约库
- 实现了重入攻击防护
- 价格预言机包含心跳检查，防止使用过时数据
- 多重签名机制保护关键操作
- 紧急暂停功能应对突发安全事件

## 📜 许可证
MIT

## ⚠️ 免责声明
本项目仅用于演示和教育目的，未经审计，不建议在生产环境中使用。使用前请自行评估风险。

## 🚀 开始使用

### 前提条件

- Node.js 和 Yarn
- Foundry工具链
- Chainlink CCIP和Functions订阅

### 安装步骤

1. 克隆仓库
```bash
git clone https://github.com/Joe-Goldbug/ERC1155-RealEstate.git
```

2. 安装依赖
```bash
yarn install
forge install
```

3. 编译合约
```bash
forge build
```
<br><br><br><br>
<p align="center">
<strong>
感谢你阅读全文，希望这篇文档能给你带来一些帮助！<br>
作者： Joe-Goldbug<br>
联系方式: whitepeace567@gmail.com<br>
</strong>
