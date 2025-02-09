## 开通@open

> 仅阿里云服务空间支持

目前可以在uniCloud web控制台购买redis服务，**所购买的实例由阿里云提供，并非由DCloud提供，DCloud只提供购买入口**

1. 登录[uniCloud web控制台](https://unicloud.dcloud.net.cn/)
2. 选择一个**阿里云**服务空间
3. 选择左侧redis菜单，选择实例并购买即可

![](https://vkceyugu.cdn.bspapp.com/VKCEYUGU-f184e7c3-1912-41b2-b81f-435d1b37c7b4/3a29e715-827d-43bb-b61b-fcff71cb42f6.jpg)

**注意**

- 开通的redis实例会自动和当前服务空间绑定
- 后续可以对redis实例升配降配，请阅读下方升配降配的说明
- 购买redis实例时，选择较长的”购买时长“可以享受更多的折扣
- 付费后，需要等待3-5分钟redis实例才能初始化完成

## 规格说明@type

|规格				|CPU核数|每秒新建连接数上限	|连接数上限	|带宽（MB/s）	|QPS参考值|
|--					|--			|--									|--					|--						|--				|
|256MB主从版|2			|10,000							|10,000			|10						|80,000		|
|1GB主从版	|2			|10,000							|10,000			|10						|80,000		|
|2GB主从版	|2			|10,000							|10,000			|16						|80,000		|
|4GB主从版	|2			|10,000							|10,000			|24						|80,000		|
|8GB主从版	|2			|10,000							|10,000			|24						|80,000		|

## 费用说明@fee

### 续费@renew

在uniCloud web控制台redis详情页面可以对redis实例进行续费操作。

![](https://vkceyugu.cdn.bspapp.com/VKCEYUGU-f184e7c3-1912-41b2-b81f-435d1b37c7b4/d848dd0a-15aa-46ec-89f9-84ade9721246.jpg)

实例到期后的第1~7天，实例状态为被禁用，无法被访问。如需继续使用，您需要及时为实例续费

实例处于被禁用状态后，以您执行续费操作的时间为起点计算包年包月时长，例如您的实例在2021年04月10日到期，在2021年04月15日执行手动续费1个月的操作，那么实例的到期时间即为2021年5月15日。

### 升配@upgrade

在uniCloud web控制台redis详情页面可以对redis实例进行升配操作。升级配置需要按照剩余时间补足差额

升级实例配置所需费用 =（升级后实例每天的价格 - 升级前实例每天的价格）× 服务到期的剩余天数，具体费用以web控制台显示为准

**注意**

- 配置变更将会产生切换操作而带来1-2次30秒内的闪断，建议您在业务低峰期发起变配，避免影响业务。

### 降配@downgrade

在uniCloud web控制台redis详情页面可以对redis实例进行降配操作。

**目前可以降配但是无法退还费用到您的账号**

降配时可以选择以下两种方式

- 立即降配：实时操作降配。
- 自动降配：开启自动降配，系统会在到期当天凌晨进行降配操作。


**注意**

- 配置变更将会产生切换操作而带来1-2次30秒内的闪断，建议您在业务低峰期发起变配，避免影响业务。
- 如果降配时内存用量超过降配目标规格的内存上限，则会导致降配失败

## 在云函数中使用

如何在云函数中使用redis，请参考[扩展能力Redis](uniCloud/redis.md)

## FAQ

- 为什么刚开通的redis实例就用了几十MB内存

  redis基础服务会占用一定的内存，大小在32MB-64MB之间