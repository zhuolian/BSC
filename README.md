# BSC全能分红代币合约
支持分红SHIB/ETH/USDT/DOGE等BSC所有代币。

源码：
https://github.com/zhuolian/BSC/blob/main/FenHong.sol

如果遇到问题可联系TG：
https://t.me/hanzhuocheng

TG电报群交流群
https://t.me/

# 图文教程

# 第01步：安装小狐狸钱包

安装教程：https://www.jinse.com/news/blockchain/998480.html?ivk_sa=1024320u

# 第02步：在小狐狸钱包添加主网节点

1.网络名称：BSC

2.RPC 网址：https://bsc-dataseed3.binance.org/

3.链ID：56

4.货币符号：BNB

5.主网浏览器：https://bscscan.com/

6.部署主网去交易所购买BNB币

# 第03步：打开Remix：https://remix.ethereum.org

1.点击GitHub

![1](https://github.com/zhuolian/BSC/blob/main/images/01.png)

2.输入合约地址

https://github.com/zhuolian/BSC/blob/main/FenHong.sol

3.点击 “import”

![2](https://github.com/zhuolian/BSC/blob/main/images/02.png)

4.选择 FenHong.sol

![3](https://github.com/zhuolian/BSC/blob/main/images/03.png)

# 第04步：编译部署

1.点击编译

2.COMPILER：选择 “v0.8.7+commit.e28d00a7.js”

3.LANGUAGE：选择 “Solidity”

4.EVM VERSION：选择 “default”

5.COMPILER CONFIGURATION：勾选 “Auto compile”，同时勾选 “Enable optimization”，200

6.点击 “Compile FenHong.sol” 开始编译

![4](https://github.com/zhuolian/BSC/blob/main/images/04.png)

7.选择 “FenHong.sol”

![5](https://github.com/zhuolian/BSC/blob/main/images/05.png)

# 第05步：部署参数

1.ENVIRONMENT：Injected Web3（部署环境）

2.ACCOUNT：（合约部署账户，连接小狐狸钱包币安主网钱包地址）

3.Value：200000000000000000 (2后面+17个0)（0.2BNB）

4.NAME_: FenHong（填写代币名称）

5.symbol_: FH （填写代币简称）

6.TOTALSUPPLY_: 100000000(发行总量，发多少就写多少)

7.REWARDADDR_:(要分红的代币合约，分红哪个代币，就填哪个代币的合约地址)

注意：不能分红BNB和WBNB，因为现在WBNB也不走薄饼交易所了

BSC常用代币合约如下：

SHIB的合约地址: 0x2859e4544C4bB03966803b044A93563Bd2D0DD4D

USDT合约地址:0x55d398326f99059fF775485246999027B3197955

ETH的合约地址: 0x2170Ed0880ac9A755fd29B2688956BD959F933F8 

DOGE的合约地址: 0xbA2aE424d960c26247Dd6c32edC70B295c744C43 

BUSD的合约地址: 0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56 

CAKE的合约地址: 0x0E09FaBB73Bd3Ade0a17ECC321fD13a19e81cE82 

8.MARKETINGWALLETADDR_:(填写自己的市场营销钱包地址) 

9.BUYFEESETTING_:[4,3,2,1]，买入收取手续费比例：分别为(分红、流动性、市场营销、销毁燃烧)

10.SELLFEESETTING_: [5,4,3,2]，卖出收取手续费比例：分别为(分红、流动性、市场营销、销毁燃烧)

注意：上述四个手续费参数可以任意设置，但是总和不能超过25%，例如[10,10,10,10]总和为40%，部署就会失败。

11.TOKENBALANCEFORREWARD_: 1000000000000000000(1后面+18个0)，持有多少代币以上才会参与分红。

注意：持有代币即可分红：填1后面+18个0，如持有10亿以上代币才可以分红，填10亿+18个0，因为代币的精度是18。

12.点击 “stansact” 开始部署

![6](https://github.com/zhuolian/BSC/blob/main/images/06.png)

