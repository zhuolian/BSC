#第01步：安装小狐狸钱包

安装教程：https://www.jinse.com/news/blockchain/998480.html?ivk_sa=1024320u

第02步：添加网络节点

1)在小狐狸钱包中添加币安测试网节点  

网络名称：BSC TestNet

RPC 网址：https://data-seed-：prebsc-1-s1.binance.org:8545/

链ID：97

货币符号：BNB

测试网浏览器：https://testnet.bscscan.com/	

去水龙头领取测试币：https://testnet.binance.org/faucet-smart

2)在小狐狸钱包中添加币安主网节点
网络名称：BSC
RPC 网址：https://bsc-dataseed3.binance.org/
链ID：56
货币符号：BNB
主网浏览器：https://bscscan.com/
部署主网去交易所购买BNB币

第03步：编译部署
打开线编译工具：https://remix.ethereum.org/

第04步：新建一个文件 — 把源码拷贝进来
第05步：修改源码路由地址
第868行（二选一）
1）部署测试网，请使用括号中的测试网路由地址
IUniswapV2Router02 _uniswapV2Router = IUniswapV2Router02(0xB6BA90af76D139AB3170c7df0139636dB6120F7e);
2）部署主网，请使用括号中的主网路由地址
IUniswapV2Router02 _uniswapV2Router = IUniswapV2Router02(0x10ED43C718714eb63d5aA57B78B54704E256024E);

4、部署参数
1）代币名称：NAME_: FenHong Token
2）代币符号：SYMBOL_: FenHong
3）发行总量：TOTALSUPPLY_: 1000000000000000(1000万亿)
4）要分红的代币合约：REWARDADDR_:
分红哪个代币，就填哪个代币的合约地址，BSC常用代币合约如下：
SHIB测试网合约地址:0x11e815a78Cc41D733Db00f06B3A96074855362CE
USDT测试网合约地址:0xEdA5dA0050e21e9E34fadb1075986Af1370c7BDb
ETH测试网合约地址:  
DOGE测试网合约地址: 
BUSD测试网合约地址:  
CAKE测试网合约地址: 
5）市场营销钱包地址： MARKETINGWALLETADDR_: 
6）买入收取手续费比例：BUYFEESETTING_: [分红,流动性,市场营销,销毁燃烧][4,3,2,1]
8）卖出收取手续费比例：SELLFEESETTING_: [分红,流动性,市场营销,销毁燃烧][5,4,3,2]
注意：上述四个手续费参数可以任意设置，但是总和不能超过25%，例如[10,10,10,10]总和为40%，部署就会失败。
9）持有多少代币以上才会参与分红：TOKENBALANCEFORREWARD_: 1000000000000000000(1后面+18个0)
注意：持有代币即可分红：填1+18个0，如持有10亿以上代币才可以分红，填10亿+18个0，因为代币的精度是18
5、部署费用
VALUE: 200000000000000000 (2后面+17个0)
这个代币（合约）是一个收费（部署）的合约，直接点击部署，会报错，提示：没有足够的手续费，
部署这个合约需要0.2BNB，如果转换成wei这个单位，就是2后面+17个0，即：200000000000000000wei=0.2BNB

BSC全能分红代币合约
支持分红SHIB/ETH/USDT/DOGE等BSC所有代币。

源码：
https://github.com/tmimehi/dividendcontract/blob/main/dividendcontract.sol

如果遇到问题可联系TG：
https://t.me/zvx_Staff

TG电报群交流群
https://t.me/ZVX_Official

Remix
https://remix.ethereum.org/

编译/开源参数
COMPILER: v0.8.7+commit.e28d00a7.js

Enable optimization: 开启并使用默认值200

Other Settings: default evmVersion, MIT license

部署参数
Value填写：200000000000000000 （0.2BNB）

CONTRACT 选择 dividendcontract，

name_: BTC COIN (代币名称)

symbol_: BTC (代币简称)

totalSupply_: 21000000 (发行量 发多少就写多少)

rewardAddr_: 要分红的代币合约，BSC常用代币地址在下方

marketingWalletAddr_: 你自己的营销钱包地址

buyFeeSetting_: [4,3,2,1] (分红、流动性、营销钱包、燃烧)

sellFeeSetting_: [5,4,3,2] (分红、流动性、营销钱包、燃烧)

tokenBalanceForReward_: 10000000000000000000000 (持有多少代币参与分红。数量后要加18个0)

BSC常用代币合约地址 不能分红BNB和wbnb 因为现在WBNB也不走薄饼交易所了
SHIB: 0x2859e4544C4bB03966803b044A93563Bd2D0DD4D

USDT: 0x55d398326f99059fF775485246999027B3197955

ETH: 0x2170Ed0880ac9A755fd29B2688956BD959F933F8

DOGE: 0xbA2aE424d960c26247Dd6c32edC70B295c744C43

BUSD: 0xe9e7CEA3DedcA5984780Bafc599bD69ADd087D56

CAKE: 0x0E09FaBB73Bd3Ade0a17ECC321fD13a19e81cE82

图文教程
1，打开Remix：https://remix.ethereum.org

2，点击GitHub

1

3，输入合约地址

https://github.com/tmimehi/dividendcontract/blob/main/dividendcontract.sol

4，点击import

5，选择dividendcontract.sol

2

6，点击编译

7，选择编译版本0.8.7

9，点击 编辑

3

10,选择dividendcontract

4

11,ENVIRONMENT选择：injected Web3

VALUE输入：200000000000000000

name_: BTC COIN (代币名称)

symbol_: BTC (代币简称)

totalSupply_: 21000000 (发行量 发多少就写多少)

rewardAddr_: 要分红的代币合约，BSC常用代币地址在下方

marketingWalletAddr_: 你自己的营销钱包地址

buyFeeSetting_: [4,3,2,1] (分红、流动性、营销钱包、燃烧)

sellFeeSetting_: [5,4,3,2] (分红、流动性、营销钱包、燃烧)

tokenBalanceForReward_: 10000000000000000000000 (持有多少代币参与分红。数量后要加18个0)

5

12，点击 transact 

13，小狐狸钱包点击确认

6

14，等待几十秒，你的代币合约将出现在REdmix右下角

7
