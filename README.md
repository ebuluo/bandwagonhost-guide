# 搬瓦工（BandwagonHost）选购与使用指南

如果你刚接触海外服务器，很大概率会经常看到别人聊起“搬瓦工”。它隶属于加拿大主机商 IT7 Networks Inc.，属于典型的自管型（Unmanaged）KVM VPS。简单说就是机房硬件、电源和主干网由他们维护，系统安装、网站搭建、环境配置和日常数据备份都得自己动手。

你可以直接访问 [搬瓦工官网](https://bandwagonhost.com/aff.php?aff=68446) 浏览所有服务。在掏钱包之前，建议先花几分钟搞清楚它的线路特点、不同机房的差价原因以及自己的真实需求，避免花了大价钱却买到不适合自己的配置。

---

## 搬瓦工到底贵在哪？

很多新手第一眼看到搬瓦工的价格都会觉得偏贵，尤其是对比那些一年只要十几美元的普通便宜机器。搬瓦工现在几乎不做超低价机器，它的溢价主要集中在跨国回国线路的质量上。

普通海外服务器走的是公共国际互联网路由，平时访问尚可，一到晚上八九点跨国流量高峰期就会出现丢包严重、延迟忽高忽低的情况。搬瓦工通过接入电信 CN2 GIA、联通 9929/AS10099 以及移动 CMIN2 等优化线路，在跨国主干网上买了更高等级的带宽保障。

此外，他们自己开发的 KiwiVM 面板功能很直观，点几下就能重装系统、切换机房或者恢复快照，对不喜欢命令行折腾后台的人很省心。但这不代表它适合所有人；如果你的网站主要面对欧美本地访客，买普通线路的海外服务器就足够好，没必要为回国优质带宽多花几倍钱。

---

## 选机房前，先把网络线路看明白

搬瓦工目前在全球 11 个城市提供了 20 个机房节点，但不同套餐能够使用的机房范围差异很大。买之前一定要明白：套餐自带什么机房权限，决定了你以后能不能在后台随时切换过去。

### 1. 电信 CN2 GIA、联通 9929 与移动 CMIN2
这是搬瓦工最受欢迎的网络组合，通常出现在洛杉矶 DC6（USCA_6）、洛杉矶 DC9（USCA_9）、日本东京（JPTY_8）、日本大阪（JPOS_6）以及香港（HK_8）等机房。

- **电信 CN2 GIA**：中国电信的高等级专线，晚高峰走专属通道，丢包率相对很低，跨国访问延迟稳定。
- **联通 Premium（AS10099 / 9929）**：联通的高端回国线路，在北方和沿海地区连接欧美机房时表现尤其顺畅。
- **移动 CMIN2**：中国移动自己的高质量跨国通道，有效缓解了过去普通移动宽带晚高峰连海外严重堵车的问题。

虽然这些线路在绝大多数时候都能保持低延迟和较好的速度，但依然属于跨国公网连接，遇到海底光缆维护或上游骨干波动时同样会有短暂影响，没有任何服务商能保证 24 小时绝对不波动。

### 2. 日本软银（Softbank）与普通海外直连
日本软银线路主要设在大阪（JPOS_1）和东京（JPTY_1）机房。中国联通用户直连软银的效果通常非常优秀，甚至延迟能控制在很低的水平；但对于电信和部分移动用户来说，晚高峰可能会有波动，不如直接上 CN2 GIA 省心。

普通线路则包括弗里蒙特（USCA_FMT）、洛杉矶普通节点（USCA_2）、纽约（USNY_6）以及阿姆斯特丹（EUNL_2）。这些机房价格亲民，非常适合面向欧美本地的英文博客、外贸展示网站或者跑一些不需要低延迟回国的后台测试任务。

### 3. 香港、东京、大阪与新加坡独立机房
在搬瓦工的产品线里，这几个亚洲机房属于独立套餐，不与普通洛杉矶套餐混用。它们的物理距离距离国内最近，延迟甚至可以媲美境内主机，但亚洲高等级带宽极其昂贵，因此每月的费用和流量单价都会比北美机房高出一大截。

---

## 第一次买，挑哪款最合算？

挑机器的第一步不是比配置，而是明确你的预算、主要访客群体以及你本地的宽带网络。

如果你的主要需求是个人测试、跑脚本，或者搭建一个访客基本在海外的外贸站点，直接选择 **常规 KVM** 系列即可。它的门槛最低，年付 49.99 美元起步，给足了常规建站所需的磁盘与流量，性价比最高。

如果你需要国内访问速度快、连接稳定，最均衡的选择是 **CN2 GIA E-Commerce** 系列（通常推荐从洛杉矶 DC6 或 DC9 起步）。这个系列同时覆盖了电信、联通和移动的三网回国优化，哪怕以后发现当地网络走洛杉矶不够理想，也可以在面板里自由切换到加拿大、荷兰或日本软银等多达 15 个机房。

如果你对延迟有极其苛刻的要求，比如需要实时交互的业务，且预算非常充裕，再考虑 **香港**、**东京** 或 **大阪** 的 CN2 GIA 套餐。对于绝大多数个人和中小站点，北美 CN2 GIA 的速度已经完全够用，不需要盲目追求上百美元一个月的亚洲机房。

至于 **限量版与特别版**，这类套餐往往带有特定机房限制或较低的年付价格，但平时官网大多处于缺货状态。如果碰巧遇到补货，且配置和线路正好匹配你的需求，可以作为高性价比备选。

---

## 付款周期怎么选：年付还是季度付？

搬瓦工支持月付、季度付、半年付和年付（部分低配或限量套餐仅支持年付）。

对于刚刚接触搬瓦工的新人，如果选择的套餐支持季度付，建议第一次先买一个季度试用。因为各地的家庭宽带与公司网络情况不同，自己实测一到两周晚高峰的实际使用感受，远比看网上的理论参数更稳妥；如果用得顺手，后续出账单时再改为年付也不迟。

年付的优势在于单月折算下来最便宜，能省下不少预算，但缺点是一次性掏出的资金较多。需要注意的是，只要不是特别差钱，不要为了省一点点钱而强行买不符合需求的年付低配机器，按需选择才能避免浪费。

---

## 搬瓦工 78 款套餐完整价格表

价格和库存以官网下单页为准。

### 常规 KVM（6 款）

这是搬瓦工门槛最低的系列，包含 5 个基础海外机房（温哥华、阿姆斯特丹、弗里蒙特、洛杉矶普通节点和纽约）。虽然没有专门的三网优化回国直连，但机器配置很给力，磁盘和基础流量都给得很足，非常适合做海外业务站、自动化任务或离线备份。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 20G KVM · **PID 44** | 2 核 / 1 GB | 20 GB | 1000 GB / 1 Gbps | $49.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=44&billingcycle=annually) |
| 40G KVM · **PID 45** | 3 核 / 2 GB | 40 GB | 2000 GB / 1 Gbps | $52.99 / 半年<br>$99.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=45&billingcycle=annually) |
| 80G KVM · **PID 46** | 4 核 / 4 GB | 80 GB | 3000 GB / 1 Gbps | $19.99 / 月<br>$59.99 / 季度<br>$107.99 / 半年<br>$199.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=46&billingcycle=annually) |
| 160G KVM · **PID 47** | 5 核 / 8 GB | 160 GB | 4000 GB / 1 Gbps | $39.99 / 月<br>$112.99 / 季度<br>$213.99 / 半年<br>$399.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=47&billingcycle=annually) |
| 320G KVM · **PID 48** | 6 核 / 16 GB | 320 GB | 5000 GB / 1 Gbps | $79.99 / 月<br>$227.99 / 季度<br>$432.99 / 半年<br>$799.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=48&billingcycle=annually) |
| 480G KVM · **PID 49** | 7 核 / 24 GB | 480 GB | 6000 GB / 1 Gbps | $119.99 / 月<br>$341.99 / 季度<br>$649.49 / 半年<br>$1,199.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=49&billingcycle=annually) |

### CN2 GIA E-Commerce（9 款）

最受欢迎的拳头系列，自带 15 个可选机房权限。默认可以选择洛杉矶 DC6（USCA_6）或 DC9（USCA_9），具备高达 2.5Gbps 到 10Gbps 的网络端口，同时兼顾了电信 CN2 GIA、联通 9929 与移动 CMIN2，是国内访问综合体验最均衡的方案。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 20G CN2 GIA ECOMMERCE · **PID 87** | 2 核 / 1 GB | 20 GB | 1000 GB / 2.5 Gbps | $49.99 / 季度<br>$89.99 / 半年<br>$169.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=87&billingcycle=annually) |
| 40G CN2 GIA ECOMMERCE · **PID 88** | 3 核 / 2 GB | 40 GB | 2000 GB / 2.5 Gbps | $89.99 / 季度<br>$169.99 / 半年<br>$299.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=88&billingcycle=annually) |
| 80G CN2 GIA ECOMMERCE · **PID 89** | 4 核 / 4 GB | 80 GB | 3000 GB / 2.5 Gbps | $56.99 / 月<br>$149.99 / 季度<br>$289.99 / 半年<br>$549.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=89&billingcycle=annually) |
| 160G CN2 GIA ECOMMERCE · **PID 90** | 6 核 / 8 GB | 160 GB | 5000 GB / 5 Gbps | $86.99 / 月<br>$239.99 / 季度<br>$459.99 / 半年<br>$879.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=90&billingcycle=annually) |
| 320G CN2 GIA ECOMMERCE · **PID 91** | 8 核 / 16 GB | 320 GB | 8000 GB / 5 Gbps | $159.99 / 月<br>$459.99 / 季度<br>$869.99 / 半年<br>$1,599.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=91&billingcycle=annually) |
| 640G CN2 GIA ECOMMERCE · **PID 92** | 10 核 / 31.9121 GB | 640 GB | 10000 GB / 10 Gbps | $289.99 / 月<br>$799.99 / 季度<br>$1,499.99 / 半年<br>$2,759.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=92&billingcycle=annually) |
| 1280G CN2 GIA ECOMMERCE · **PID 93** | 12 核 / 64 GB | 1280 GB | 12000 GB / 10 Gbps | $549.99 / 月<br>$1,559.99 / 季度<br>$2,979.99 / 半年<br>$5,499.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=93&billingcycle=annually) |
| 1280G CN2 GIA ECOMMERCE HIBW 15T · **PID 160** | 12 核 / 64 GB | 1280 GB | 15000 GB / 10 Gbps | $679.00 / 月<br>$1,935.00 / 季度<br>$3,670.00 / 半年<br>$6,790.00 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=160&billingcycle=annually) |
| 1280G CN2 GIA ECOMMERCE HIBW 20T · **PID 161** | 12 核 / 64 GB | 1280 GB | 20000 GB / 10 Gbps | $899.00 / 月<br>$2,562.00 / 季度<br>$4,860.00 / 半年<br>$8,999.00 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=161&billingcycle=annually) |

### E-Commerce + SLA（9 款）

该系列固定在洛杉矶 USCA_5 机房，带有明确的 99.99% 月可用性 SLA 协议。不同于常规套餐有严格的一小时平均 CPU 占用限制，SLA 系列允许全部可用核心 24/7 长时间满载，适合需要不间断高负荷计算、编译或严格运行保障的用户。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 20G KVM - ECOMMERCE SLA LOS ANGELES · **PID 164** | 2 核 / 1.03516 GB | 20 GB | 1000 GB / 2.5 Gbps | $65.89 / 季度<br>$125.99 / 半年<br>$239.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=164&billingcycle=annually) |
| 40G KVM - ECOMMERCE SLA LOS ANGELES · **PID 165** | 3 核 / 2.04297 GB | 40 GB | 2000 GB / 2.5 Gbps | $116.99 / 季度<br>$219.99 / 半年<br>$399.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=165&billingcycle=annually) |
| 80G KVM - ECOMMERCE SLA LOS ANGELES · **PID 166** | 4 核 / 4.04297 GB | 80 GB | 3000 GB / 2.5 Gbps | $69.99 / 月<br>$199.99 / 季度<br>$379.99 / 半年<br>$699.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=166&billingcycle=annually) |
| 160G KVM - ECOMMERCE SLA LOS ANGELES · **PID 167** | 6 核 / 8.0625 GB | 160 GB | 5000 GB / 5 Gbps | $109.99 / 月<br>$299.99 / 季度<br>$569.99 / 半年<br>$1,099.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=167&billingcycle=annually) |
| 320G KVM - ECOMMERCE SLA LOS ANGELES · **PID 168** | 8 核 / 16.125 GB | 320 GB | 8000 GB / 5 Gbps | $199.99 / 月<br>$569.99 / 季度<br>$1,079.99 / 半年<br>$1,999.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=168&billingcycle=annually) |
| 640G KVM - ECOMMERCE SLA LOS ANGELES · **PID 169** | 10 核 / 32.1621 GB | 640 GB | 10000 GB / 10 Gbps | $369.99 / 月<br>$1,055.99 / 季度<br>$1,999.99 / 半年<br>$3,699.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=169&billingcycle=annually) |
| 1280G KVM - ECOMMERCE SLA LOS ANGELES · **PID 170** | 12 核 / 64 GB | 1280 GB | 12000 GB / 10 Gbps | $699.99 / 月<br>$1,989.99 / 季度<br>$3,779.99 / 半年<br>$6,999.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=170&billingcycle=annually) |
| 1280G KVM - ECOMMERCE SLA LOS ANGELES HIBW 15T · **PID 171** | 12 核 / 64 GB | 1280 GB | 15000 GB / 10 Gbps | $879.99 / 月<br>$2,509.99 / 季度<br>$4,768.99 / 半年<br>$8,799.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=171&billingcycle=annually) |
| 1280G KVM - ECOMMERCE SLA LOS ANGELES HIBW 20T · **PID 172** | 12 核 / 64 GB | 1280 GB | 20000 GB / 10 Gbps | $1,159.99 / 月<br>$3,299.99 / 季度<br>$6,269.99 / 半年<br>$11,598.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=172&billingcycle=annually) |

### 香港 CN2 GIA（6 款）

香港机房（HK_8）接入 Equinix 设施，直连电信 CN2 GIA 回国。到国内大部分城市的 ping 延迟可以低至 30~50ms，几乎感受不到跨国网络的存在，但价格也是所有系列里最昂贵的，适合对延迟极其敏感且预算充裕的业务。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 40G HONG KONG CN2 GIA · **PID 95** | 2 核 / 2 GB | 40 GB | 500 GB / 1 Gbps | $89.99 / 月<br>$249.99 / 季度<br>$479.99 / 半年<br>$899.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=95&billingcycle=annually) |
| 80G HONG KONG CN2 GIA · **PID 96** | 4 核 / 4 GB | 80 GB | 1000 GB / 1 Gbps | $155.99 / 月<br>$439.99 / 季度<br>$829.99 / 半年<br>$1,559.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=96&billingcycle=annually) |
| 160G HONG KONG CN2 GIA · **PID 97** | 6 核 / 8 GB | 160 GB | 2000 GB / 1 Gbps | $299.99 / 月<br>$859.99 / 季度<br>$1,599.99 / 半年<br>$2,999.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=97&billingcycle=annually) |
| 320G HONG KONG CN2 GIA · **PID 98** | 8 核 / 16 GB | 320 GB | 4000 GB / 1 Gbps | $589.99 / 月<br>$1,669.99 / 季度<br>$3,169.99 / 半年<br>$5,899.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=98&billingcycle=annually) |
| 640G HONG KONG CN2 GIA · **PID 122** | 10 核 / 32 GB | 640 GB | 6000 GB / 1 Gbps | $989.99 / 月<br>$2,819.99 / 季度<br>$5,289.99 / 半年<br>$9,989.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=122&billingcycle=annually) |
| 1280G HONG KONG CN2 GIA · **PID 124** | 12 核 / 64 GB | 1280 GB | 8000 GB / 1 Gbps | $1,889.99 / 月<br>$5,389.99 / 季度<br>$9,989.99 / 半年<br>$18,989.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=124&billingcycle=annually) |

### 东京 CN2 GIA（6 款）

东京 JPTY_8 机房同样拥有顶级配置与 CN2 GIA 直连，端口为 1.2Gbps。对于我国华东、华北沿海地区来说，东京的物理连接非常快速平稳，但费用与香港系列基本持平，属于高端定位。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 40G TOKYO CN2 GIA · **PID 108** | 2 核 / 2 GB | 40 GB | 500 GB / 1.2 Gbps | $89.99 / 月<br>$249.99 / 季度<br>$479.99 / 半年<br>$899.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=108&billingcycle=annually) |
| 80G TOKYO CN2 GIA · **PID 109** | 4 核 / 4 GB | 80 GB | 1000 GB / 1.2 Gbps | $155.99 / 月<br>$439.99 / 季度<br>$829.99 / 半年<br>$1,559.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=109&billingcycle=annually) |
| 160G TOKYO CN2 GIA · **PID 110** | 6 核 / 8 GB | 160 GB | 2000 GB / 1.2 Gbps | $299.99 / 月<br>$859.99 / 季度<br>$1,599.99 / 半年<br>$2,999.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=110&billingcycle=annually) |
| 320G TOKYO CN2 GIA · **PID 111** | 8 核 / 16 GB | 320 GB | 4000 GB / 1.2 Gbps | $589.99 / 月<br>$1,669.99 / 季度<br>$3,169.99 / 半年<br>$5,899.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=111&billingcycle=annually) |
| 640G TOKYO CN2 GIA · **PID 123** | 10 核 / 32 GB | 640 GB | 6000 GB / 1.2 Gbps | $989.99 / 月<br>$2,819.99 / 季度<br>$5,289.99 / 半年<br>$9,989.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=123&billingcycle=annually) |
| 1280G TOKYO CN2 GIA · **PID 125** | 12 核 / 64 GB | 1280 GB | 8000 GB / 1.2 Gbps | $1,889.99 / 月<br>$5,389.99 / 季度<br>$9,989.99 / 半年<br>$18,989.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=125&billingcycle=annually) |

### 大阪 CN2 GIA（6 款）

大阪 JPOS_6 机房同样提供 CN2 GIA 直连，但月费定价相比东京和香港大幅降低，月付 49.99 美元起步。对于既想要日本低延迟线路、又觉得东京套餐价格太高的人来说，大阪 CN2 GIA 是一个性价比高得多的折中选项。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 40G OSAKA CN2 GIA · **PID 134** | 2 核 / 2 GB | 40 GB | 500 GB / 1.5 Gbps | $49.99 / 月<br>$139.99 / 季度<br>$269.99 / 半年<br>$499.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=134&billingcycle=annually) |
| 80G OSAKA CN2 GIA · **PID 135** | 4 核 / 4 GB | 80 GB | 1000 GB / 1.5 Gbps | $86.99 / 月<br>$245.99 / 季度<br>$459.99 / 半年<br>$869.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=135&billingcycle=annually) |
| 160G OSAKA CN2 GIA · **PID 136** | 6 核 / 8 GB | 160 GB | 2000 GB / 1.5 Gbps | $165.99 / 月<br>$479.99 / 季度<br>$888.99 / 半年<br>$1,665.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=136&billingcycle=annually) |
| 320G OSAKA CN2 GIA · **PID 137** | 8 核 / 16 GB | 320 GB | 4000 GB / 1.5 Gbps | $329.99 / 月<br>$929.99 / 季度<br>$1,739.99 / 半年<br>$3,199.00 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=137&billingcycle=annually) |
| 640G OSAKA CN2 GIA · **PID 138** | 10 核 / 32 GB | 640 GB | 6000 GB / 1.5 Gbps | $549.99 / 月<br>$1,569.99 / 季度<br>$2,939.99 / 半年<br>$5,549.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=138&billingcycle=annually) |
| 1280G OSAKA CN2 GIA · **PID 139** | 12 核 / 64 GB | 1280 GB | 8000 GB / 1.5 Gbps | $1,059.99 / 月<br>$2,999.99 / 季度<br>$5,559.99 / 半年<br>$10,559.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=139&billingcycle=annually) |

### 新加坡 CN2 GIA（6 款）

新加坡 SG_8 机房兼顾了东南亚本地直连与中国电信 CN2 GIA、移动 CMIN2。对于主要客户群分布在东南亚以及中国南部沿海的跨国业务，新加坡机房在物理跳数和访问响应上都有独到的地理优势。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 40G SINGAPORE CN2 GIA · **PID 173** | 2 核 / 2 GB | 40 GB | 500 GB / 1.5 Gbps | $49.99 / 月<br>$139.99 / 季度<br>$269.99 / 半年<br>$499.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=173&billingcycle=annually) |
| 80G SINGAPORE CN2 GIA · **PID 174** | 4 核 / 4 GB | 80 GB | 1000 GB / 1.5 Gbps | $86.99 / 月<br>$245.99 / 季度<br>$459.99 / 半年<br>$869.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=174&billingcycle=annually) |
| 160G SINGAPORE CN2 GIA · **PID 175** | 6 核 / 8 GB | 160 GB | 2000 GB / 2.5 Gbps | $165.99 / 月<br>$479.99 / 季度<br>$888.99 / 半年<br>$1,665.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=175&billingcycle=annually) |
| 320G SINGAPORE CN2 GIA · **PID 176** | 8 核 / 16 GB | 320 GB | 4000 GB / 2.5 Gbps | $329.99 / 月<br>$929.99 / 季度<br>$1,739.99 / 半年<br>$3,199.00 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=176&billingcycle=annually) |
| 640G SINGAPORE CN2 GIA · **PID 177** | 10 核 / 32 GB | 640 GB | 6000 GB / 5 Gbps | $549.99 / 月<br>$1,569.99 / 季度<br>$2,939.99 / 半年<br>$5,549.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=177&billingcycle=annually) |
| 1280G SINGAPORE CN2 GIA · **PID 178** | 12 核 / 64 GB | 1280 GB | 8000 GB / 5 Gbps | $1,059.99 / 月<br>$2,999.99 / 季度<br>$5,559.99 / 半年<br>$10,559.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=178&billingcycle=annually) |

### 迪拜 E-Commerce（7 款）

迪拜 AEDXB_1 机房直连中东本地主要运营商（DU 与 Etisalat）。如果你需要开拓中东阿联酋及海湾地区的外贸建站、API 接口或本地化服务，选择这个节点比绕道欧洲或新加坡要有更低的物理延迟。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| 20G DUBAI - ECOMMERCE · **PID 114** | 2 核 / 1 GB | 20 GB | 500 GB / 1 Gbps | $19.99 / 月<br>$49.99 / 季度<br>$89.99 / 半年<br>$169.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=114&billingcycle=annually) |
| 40G DUBAI - ECOMMERCE · **PID 115** | 3 核 / 2 GB | 40 GB | 1000 GB / 1 Gbps | $32.99 / 月<br>$89.99 / 季度<br>$169.99 / 半年<br>$299.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=115&billingcycle=annually) |
| 80G DUBAI - ECOMMERCE · **PID 116** | 4 核 / 4 GB | 80 GB | 2000 GB / 1 Gbps | $56.99 / 月<br>$149.99 / 季度<br>$289.99 / 半年<br>$549.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=116&billingcycle=annually) |
| 160G DUBAI - ECOMMERCE · **PID 117** | 6 核 / 8 GB | 160 GB | 3000 GB / 1 Gbps | $86.99 / 月<br>$239.99 / 季度<br>$459.99 / 半年<br>$879.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=117&billingcycle=annually) |
| 320G DUBAI - ECOMMERCE · **PID 118** | 8 核 / 16 GB | 320 GB | 4000 GB / 1 Gbps | $159.99 / 月<br>$459.99 / 季度<br>$869.99 / 半年<br>$1,599.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=118&billingcycle=annually) |
| 640G DUBAI - ECOMMERCE · **PID 119** | 10 核 / 32 GB | 640 GB | 5000 GB / 1 Gbps | $289.99 / 月<br>$799.99 / 季度<br>$1,499.99 / 半年<br>$2,759.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=119&billingcycle=annually) |
| 1280G DUBAI - ECOMMERCE · **PID 120** | 12 核 / 64 GB | 1280 GB | 6000 GB / 1 Gbps | $549.99 / 月<br>$1,559.99 / 季度<br>$2,979.99 / 半年<br>$5,399.99 / 年 | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=120&billingcycle=annually) |

### 限量与特别版（23 款）

官方不定期上架的促销型机器，涵盖了社区定制款（如 NodeSeek 联名）、特定单机房优惠款（如 DC9、Amsterdam、Tokyo）以及多机房漫游的 The Plan 系列。这些套餐通常只能年付，且平时基本无货，表格中的价格为官方发售参考价，适合在补货时对照配置选购。

| 套餐 / PID | CPU / 内存 | 磁盘 | 月流量 / 端口 | 各付款周期总价（USD） | 官网购买 |
| --- | --- | --- | --- | --- | --- |
| MINICHICKEN · **PID 158** | 1 核 / 1 GB | 20 GB | 1000 GB / 1 Gbps | $19.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=158&billingcycle=annually) |
| The DC9 Plan · **PID 145** | 1 核 / 768 MB | 15 GB | 750 GB / 1.5 Gbps | $38.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=145&billingcycle=annually) |
| NODESEEK-BIGGERBOX-PRO · **PID 156** | 1 核 / 1 GB | 20 GB | 1000 GB / 2.5 Gbps | $39.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=156&billingcycle=annually) |
| The Amsterdam Plan · **PID 159** | 1 核 / 1 GB | 20 GB | 1000 GB / 2.5 Gbps | $39.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=159&billingcycle=annually) |
| THE CHICKEN · **PID 130** | 1 核 / 1 GB | 20 GB | 1000 GB / 2.5 Gbps | $39.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=130&billingcycle=annually) |
| NODESEEK-MEGABOX-PRO · **PID 157** | 2 核 / 2 GB | 40 GB | 2000 GB / 2.5 Gbps | $49.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=157&billingcycle=annually) |
| 10G LOS ANGELES - CN2 GIA 限量版 · **PID 94** | 1 核 / 512 MB | 10 GB | 500 GB / 1 Gbps | $49.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=94&billingcycle=annually) |
| The DC6 Plan · **PID 149** | 1 核 / 1 GB | 20 GB | 1000 GB / 2.5 Gbps | $53.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=149&billingcycle=annually) |
| 10G JAPAN 限量版 · **PID 104** | 1 核 / 512 MB | 10 GB | 500 GB / 1 Gbps | $69.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=104&billingcycle=annually) |
| NODESEEK-SAKURA · **PID 154** | 1 核 / 1 GB | 30 GB | 500 GB / 1 Gbps | $79.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=154&billingcycle=annually) |
| The Tokyo Plan · **PID 162** | 1 核 / 1 GB | 20 GB | 500 GB / 2.5 Gbps | $79.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=162&billingcycle=annually) |
| 20G LOS ANGELES - CN2 GIA 限量版 DC9 · **PID 112** | 1 核 / 1 GB | 20 GB | 500 GB / 1 Gbps | $79.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=112&billingcycle=annually) |
| 20G HONG KONG 85 限量版 · **PID 121** | 1 核 / 1 GB | 20 GB | 500 GB / 1 Gbps | $79.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=121&billingcycle=annually) |
| 20G LOS ANGELES - CN2 GIA 限量版 DC9 · **PID 143** | 1 核 / 1 GB | 20 GB | 1000 GB / 1 Gbps | $79.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=143&billingcycle=annually) |
| 40G OSAKA 限量版 · **PID 146** | 1 核 / 2 GB | 40 GB | 2000 GB / 2.5 Gbps | $79.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=146&billingcycle=annually) |
| FREEDOM PLAN · **PID 133** | 2 核 / 2 GB | 40 GB | 2000 GB / 2.5 Gbps | $89.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=133&billingcycle=annually) |
| 20G LOS ANGELES - CN2 GIA 限量版 · **PID 132** | 2 核 / 2 GB | 40 GB | 1000 GB / 2.5 Gbps | $89.90 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=132&billingcycle=annually) |
| 20G LOS ANGELES - CN2 GIA 限量版 · **PID 105** | 1 核 / 1 GB | 20 GB | 500 GB / 1 Gbps | $89.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=105&billingcycle=annually) |
| THE PLAN · **PID 147** | 2 核 / 2 GB | 40 GB | 1000 GB / 2.5 Gbps | $99.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=147&billingcycle=annually) |
| The Tokyo Plan v2 · **PID 163** | 2 核 / 2 GB | 40 GB | 1000 GB / 5 Gbps | $99.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=163&billingcycle=annually) |
| 20G DUBAI - 限量版 · **PID 113** | 1 核 / 1 GB | 20 GB | 250 GB / 1 Gbps | $99.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=113&billingcycle=annually) |
| 20G SYDNEY 限量版 · **PID 126** | 1 核 / 1 GB | 20 GB | 500 GB / 1 Gbps | $99.99 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=126&billingcycle=annually) |
| THE PLAN v2 · **PID 131** | 2 核 / 2 GB | 40 GB | 2000 GB / 2.5 Gbps | $119.00 / 年（参考价） | [官网购买](https://bandwagonhost.com/aff.php?aff=68446&pid=131&billingcycle=annually) |

---

## 下单购买：怎么避开防欺诈拦截？

很多新手在国外主机商买机器时，经常因为填资料不当被系统判定为“欺诈订单（Fraud）”，导致付款失败。

在搬瓦工注册账号时，务必如实填写自己的个人信息，比如国家、城市、真实邮箱等，不需要也切忌故意编造假的境外地址。如果挂着代理工具导致访问 IP 和填写的国家明显不符，很容易触发官方的风控拦截。

万一订单被判定为 Fraud 也不用慌张，只要你在搬瓦工官网后台提交工单（Support Tickets），向客服如实说明情况，通常客服人工核实后就会帮你解除限制并放行订单。付款方式支持主流信用卡、PayPal 以及常见的电子支付方式，按结算页面的提示操作即可。

---

## 买完以后怎么用？KiwiVM 与首次登录

付款成功后，你会收到开通成功的通知邮件。搬瓦工所有的服务器运维操作都在专属的 KiwiVM 控制面板里完成。

### 1. 怎么进入管理后台？
登录搬瓦工官网，在顶部导航栏找到 `Services`，点击下拉菜单中的 `My Services`。在这个页面能看到你买下的 VPS 列表，点击对应机器旁边的 `Manage` 按钮，就能进入 KiwiVM 控制面板。

### 2. 重装系统与获取密码
KiwiVM 面板左侧提供了完整的功能菜单，包括开关机、强制重启、重装系统（Install new OS）以及快照备份等。如果你想换成熟悉的系统，点击 `Install new OS`，选择适合你的 Linux 发行版（如 Debian、Ubuntu 或 AlmaLinux）并确认重装。

需要注意的是，重装系统会彻底清空服务器磁盘上的所有数据，有重要文件务必提前备份。重装完成后，面板会生成临时的 root 密码，并明确标注服务器的 SSH 端口（搬瓦工通常使用随机分配的五位数端口，而不是默认的 22 端口）。

### 3. 用 SSH 客户端登录服务器
打开你常用的终端工具（如 Windows 上的 PowerShell、PuTTY，或 macOS/Linux 的 Terminal），输入远程连接命令：

```bash
ssh -p <面板显示的端口> root@<你的服务器IP>
```

例如面板显示的端口是 28419，服务器 IP 是 198.51.100.23，实际命令就是：

```bash
ssh -p 28419 root@198.51.100.23
```

回车后按提示输入面板给出的 root 密码。登录成功后，第一件事建议使用 `passwd` 命令修改为一个高强度的自定义密码，或者配置 SSH 密钥登录，提升安全性。

### 4. 机房迁移与快照
如果哪天你想换个机房试试，可以在面板左侧找到 `Migrate to another DC` 功能。系统会列出当前套餐允许切换的所有机房列表，选定后点击确认，机器会自动停机并将数据转移到新节点。迁移完成后 IP 地址会发生变化，原 IP 会被释放。

KiwiVM 还提供了免费的快照备份（Snapshots）。快照可以把你当前系统的状态完整保存下来，方便在折腾环境或者做重大升级前留个还原点。不过快照主要用来应对系统误操作回滚，不能代替把核心网站数据下载到本地的异地备份。

---

## 几个容易被忽略的使用细节

除了网络和价格，在日常使用中还有几条非常实在的规则需要留心。

### 1. CPU 核心并不是让你无休止跑满的
很多新手会误以为买了几核 CPU，就能 24 小时满载运行。搬瓦工除了带 SLA 标识的特殊套餐明确允许全部核心长时间满载外，绝大多数非 SLA 套餐都有一小时平均 CPU 限制。

比如 MINICHICKEN 套餐的单核限制是 25%，The Tokyo Plan 单核限制是 30%，The Plan 和 The Tokyo Plan v2 的平均占用限制在 45% 左右。平时编译代码、安装依赖或者网站突发访问短时间拉满没有问题，但如果长期挂载挖矿、持续压测或跑高负荷后台任务，系统检测到平均占用超标就会自动限制 CPU 频率，影响正常使用。

### 2. 退款条件的细节要求
搬瓦工支持新购 30 天内退款，但并不是无条件退款，必须同时满足以下几项硬性要求：
- 必须是新购买的机器，且处于首购 30 天以内；
- 续费产生的账单不支持退款；
- 账号状态正常，没有违规封禁；
- 系统分配给你的 IP 没有进入黑名单，且未曾因黑名单申请过更换；
- 该机器在当月的已用流量必须**严格小于 10%**（哪怕刚好达到或超过 10% 就不符合条件）；
- 过去没有恶意反复退款的记录。

### 3. 续费账单与到期处理
搬瓦工在服务器到期前 7 天会通过邮件自动生成续费账单，但官方默认不会主动从你的信用卡或 PayPal 里静默扣款。如果需要续期，你必须在到期前登录官网后台，手动完成账单支付；如果你的账户余额里提前充了值，也可以直接勾选用余额抵扣。

---

## 更多参考

如果你对海外各家主机的具体机房节点、路由走向和建站配置有更多疑问，可以在 [VPSMap](https://vpsmap.net/) 查看更多海外服务器选购与使用指南。

<!-- GEMINI_ARTICLE_COMPLETE -->
