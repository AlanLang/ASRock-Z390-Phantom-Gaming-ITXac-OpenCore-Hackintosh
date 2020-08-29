# ASRock-Z390-Phantom-Gaming-ITXac-OpenCore-Hackintosh

## 配置清单
|硬件配置|选型
|---|---|
|CPU|i7 9700k||
|主板|华擎 Z390 Phantom Gaming-ITX AC|
|显卡|蓝宝石RX560 + 显卡延长线|
|内存条|芝奇幻光戟16G * 1|
|硬盘|WD/西部数据 SN550系列500G SSD|
|电源|全汉MS600 铜牌全模组+定制线|
|无线网卡|BCM94360CD + M.2转接卡|
|散热|乔思伯240水冷|
|机箱|定制的A4机箱|

## BIOS设置
禁用如下：
| 英文 | 中文 |
| :----------------------------------- | :------------------------------------------------------- |
| Fast Boot | 快速启动 |
| CFG Lock (MSR 0xE2 write protection) | CFG 锁 (MSR 0xE2 写入保护) |

启用如下:
| 英文 | 中文 |
| :------------------- | :------------------------------------------------------- |
| Above 4G decoding | 大于 4G 地址空间解码 |
| CSM | 兼容性支持模块 |
|IGPU|IGPU多监视器|
|XHCI Hand-off|XHCI Hand-off|

注意 关于CSM看网上教程都说要关闭它，但是我关闭了之后有一定概率引导失败，所以就把它打开了

## 更新记录
### 2020年8月28日
更新OpenCore至0.6.0
更新内核扩展

### 2020年6月17日
定时USB端口，因为我所用的机箱没有前置USB端口，而主板自带了6个USB3.0，再加上一个无线网卡所以就是6*2+1=13个，小于苹果15的端口的限制，于是就把XhciPortLimit改成了false

### 2020年6月19日
升级驱动, 升级OpenCore版本至0.5.9

### 2020年6月22日
修改核显id

### 2020年6月23日
Block更名为Delete

### 2020年6月24日
由于用的博通DW1560无线网卡存在睡眠唤醒后有一定几率蓝牙不可用的情况，于是换了苹果免驱的无线网卡BCM94360CD,同时删除相关的驱动。