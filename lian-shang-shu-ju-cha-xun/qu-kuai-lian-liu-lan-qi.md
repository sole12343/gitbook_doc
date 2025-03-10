---
description: 功能强大、数据最全的多链浏览器
---

# 区块链浏览器

本区块链浏览器的优点：

* 支持多条区块链，早期支持ETH/ TRON/ BTC，未来将会支持更多区块链
* 数据展示最全的区块链，某kxlink浏览器和etherscan浏览器对于单地址能查询到的交易都有上限。\
  比如查询此地址的nft交易，其他浏览器的结果如下

[https://etherscan.io/address/0x3e57efEf507b4db7aCFa2eE79CeCA6B19e18D106#nfttransfers](https://etherscan.io/address/0x3e57efEf507b4db7aCFa2eE79CeCA6B19e18D106#nfttransfers)&#x20;

[https://www.oklink.com/zh-hans/eth/address/0x3e57efef507b4db7acfa2ee79ceca6b19e18d106/nft-transfer](https://www.oklink.com/zh-hans/eth/address/0x3e57efef507b4db7acfa2ee79ceca6b19e18d106/nft-transfer)

均无法查询到0x5634ac33e8512cdd310d4bd8747b75bfc96cb04943c2aa552f240bde69b0e276这笔nft交易，**但是在本区块链浏览器可以查询到此地址的更多2022年的交易，其他浏览器到2023年截止，无法查询到全部数据。**

* 使用简单，速度快捷，页面展示优美，中文解释清晰

### 1. 区块链浏览器首页

这是区块链浏览器的页面， 在任何其他页面时可以通过点击左侧菜单栏A区的区块链浏览器按钮，跳转到此页面

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption><p>区块链浏览器页面</p></figcaption></figure>

在C区搜索栏输入地址或者交易哈希或者区块号，默认搜索的是eth链，点击放大镜图标或者ENTER回车键，即可进入展示页面。



如果有搜索别的链的信息的需求，请在右上角点击 “切换链” 图标，之后点击你想搜索的链的logo，并在中间搜索栏输入 地址或者交易哈希或者区块号，即可进入对应链相关信息的展示页面。



### 2. 区块页面

当搜索区块号时，展示区块信息如下，包含区块的基本信息和区块内部的交易信息

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption><p>区块页面1</p></figcaption></figure>

&#x20;区块的交易信息支持跳转页面，一张页面显示10条交易，可以通过右下角进行页面切换

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>区块页面2</p></figcaption></figure>

### 3. 地址账户页面

&#x20;如果搜索地址，不论是智能合约地址还是普通用户地址，都会跳转到对应的地址页面，地址页面分为A B C三个区域，其中A区域展示的是账户当前的余额状态，此处展示的都是用户的资产情况。\
\
B区域展示的是对于此地址的重要交易信息，如果此地址是智能合约地址，那么就会展示此智能合约的开发者地址和此智能合约的创建交易，可以通过这些信息快速了解此智能合约的背景。

C区域展示的是关于此地址的全部交易情况，并且分为普通交易和代币、NFT交易。



&#x20;同样，任何时候如果想要切换区块链都需要在右上角点击对应的链图标

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>账户地址页面</p></figcaption></figure>

### 4. 交易页面

当搜索交易哈希，那么将会出现以下界面，概览界面会介绍这笔交易的全部关键信息，包含交易内部的转账和代币转账的记录。\
\
本区块链浏览器会将这笔交易的行为用通用的方式展示出来，比如说transfer swap deposite等等都用文字直接展示，方便用户理解交易的作用。

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption><p>交易界面</p></figcaption></figure>

区块链浏览器中的蓝色元素绝大多数都可以直接跳转，方便用户快速查看信息。



这是区块链浏览器的全部内容，如果想要通过sql查询区块链的信息，可以看下一章节。







