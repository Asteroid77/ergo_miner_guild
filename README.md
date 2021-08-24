# ERGO挖矿教程

## 1.准备工具

1. [NBminer](https://github.com/NebuTech/NBMiner/releases/download/v39.1/NBMiner_39.1_Win.zip)
2. [CoinEx注册](https://www.coinex.com/)

## 2.钱包地址获取

CoinEx - 资产 - 现货账户 - ERG - 充值 - 充值地址

[直达链接](https://www.coinex.com/asset/deposit?type=ERG)

## 3.设置NBminer参数

打开下载的NBminer文件夹

编辑 `start_ergo.bat`

`stratum+tcp://hk.ergo.herominers.com:10250` 改为  `stratum+tcp://ergo-jp1.nanopool.org:11111`

> 可以自行ping [挖矿地址](https://ergo.nanopool.org/)，然后拿延迟最小的那个地址替换掉，这只是普遍适用于大部分人的矿池地址。

`-u`后面`.default`之前一长串的字符串就是你的钱包地址，由步骤2得来，将你的钱包地址复制进入其中替换

`.default`则是你的矿工名，比如说我现在修改为`.Meteor`，在挖矿面板中显示的就是Meteor

`.default`后面接上`/你的邮箱地址`，该操作非常重要。矿池中修改你的最低支付币数需要这个邮箱地址来修改。如果你有多张显卡多个账户，邮箱地址也必须是一样的。

完整示例：

`nbminer -a ergo -o stratum+tcp://ergo-jp1.nanopool.org:11111 -u 9h3VYRLiCvqcwivy7j1cdtjF7D6wMcnSjibpCqBtiu2NNe7YUvp.meteor/114514@outlook.com -log`

## 4. 微星小飞机设置

实际上跟ETH的设置差不多，不想过于损耗显卡的话，自行探究功耗与算力之间的关系，每个显卡都不太一样。

我3080目前是57的功耗，不拉显存，风扇65。算力190+，每天大概0.5个币，57元/日

## 5. 提币

CoinEx - 币币交易 - 将自己获得的ERGO转换为USDT存着（当然你也可以留着赌升值），我一般都是市价抛售，你自己也可以做限价之类的操作，不多赘叙。

一般来说，都是攒了一堆USDT（100起步），然后提现（TRC20公链），转到币安/火币之类的交易所钱包中（需要手续费，所以100提一次比较划算，当然越多越好），再由币安/火币出售。

