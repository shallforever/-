软件工程大作业：多元素风格游戏
=======

# 介绍

作为《软件工程(2017)》的课程作业，我们试图使用Unity 3D 引擎开发一个多风格融合的游戏。游戏以角色扮演和关卡冒险为主要玩法，融合了生存、弹幕、射击、养成等多种元素。

开发团队成员有：

- 付宏
- 叶豪
- 牟宏杰
- 武智源
- 慕思成

本仓库包含了Unity工程的场景文件以及所有的代码文件，为了完整参与到开发进程中来，需要额外下载用到的美术资源，我们欢迎有兴趣的读者联系我们。

我们编译了V0.21b版本，读者可以到[百度网盘](https://pan.baidu.com/s/1cazXTk)下载，我们欢迎读者向我们反馈使用中遇到的任何问题。

# 更改历史

## V0.10(2017.11.19)

- 测试场景构建
- 人物构建：主角与敌人的移动控制和基本属性，敌人的仇恨机制
- 生存玩法加入：安全区会随时间缩小

## V0.11(2017.11.26)

- 重写场景生成：随机刷新障碍物与敌人，主动避开重叠位置

## V0.12(2017.11.28)

- 属性系统加入，包括等级、攻击防御、属性成长、金钱
- 加入第一个技能，按F发动，短暂的提升属性和移速，添加了简易UI
- Boss加入，融入弹幕元素，关卡获胜条件设置为击败Boss

## V0.13(2017.12.1)

- 加入Esc弹窗菜单
- 加入敌人的血条

## V0.14(2017.12.2)

- 完善了四个技能，加入了技能介绍UI，技能点设定和技能升级按钮
- Boss死后会召唤出一个商店，相关接口在shop.cs
- 游戏性数值修改；攻击键改为左Alt；缩圈时间由常数修改为10+50/回合数
- 若干Bug修复和功能改进

## V0.15(2017.12.3)

- 添加玩家属性保存和读取功能
- 修复Boss移动时进入石头中的bug
- 添加第二个关卡

## V0.16(2017.12.7)

- 在attribute中添加了两个String：NiCheng 和 ZhiYe
- 添加个人属性UI，人物死亡提示UI，商店UI框架
- 改变Esc菜单贴图，统一整体UI风格
- 添加Load动画

## V0.17(2017.12.8)

- 统一捡起、掉落物品接口
- 金币掉落增加
- 各关卡刚进入游戏时，显示弹窗，表示软件及当前关卡信息

## V0.18(2017.12.10)

- 修复若干Bug
	* 解决了经验重复获取、掉落重复生成的问题
	* 解决了四技能无法伤害Boss的问题
	* 解决了技能点可能在切换场景时消失的问题
	* 解决了UI位置偶尔会错乱的问题，统一了UI风格
- 加入角色选择功能
	* 可以选择远程角色，比近战还难打到敌人。
	* 修改了职业用词，近战称为战士，远程称为法师
	* 在主菜单加入了一个简易UI，在Safearea的Start()方法中读取所做的选择，并做出更改
- 加入背包功能
	* 加入了三种物品，分别可以立刻恢复生命值/短时间增益攻击力/短时间增益防御力
	* 物品的品质设定，每种物品有白色/绿色/蓝色/红色四种品质，具有递增的效果，总物品数达到12
	* 初步完成背包UI，在任意时刻按E呼出，可以点击一个已拥有物品，该物品选中后可以使用快捷键使用
	* 主界面加入一个物品位置，显示当前选中的背包物品及数量，按F使用物品
- 加入商店功能
	* 可以在商店中购买白色品质的三种物品
	* 十连玩法加入，高品质的物品只能抽奖获得，十连打九折，十连必出红色物品
	* 加入炫目的十连特效
- 游戏性修改
	* 复活功能加入，死亡后可以花费1000买活，否则只能重置关卡，移除了死亡时返回主菜单的功能
	* 地图上会刷出金币
	* 法师的射程是远程敌人的1.5倍
	
## V0.19(2017.12.14)

- 删除LevelSecond.unity，循环使用LevelFirst.unity
- 更改攻击按键为J
- 加入Enemy和Boss升级提升功能
- 加入文件读档和存档功能
- 加入文件数据加密功能
- 在MainMenu_server.cs中提供存档和读档的接口
- 修复若干Bug
- 扩大地形至600*600

## V0.20(2017.12.15)

- 主菜单修改：加入读取存档界面，移除多人游戏入口，替换为制作团队，背景图加了一些粒子特效
- UI更新：加入了状态图标，加入了倒计时UI，加入了技能点数量提示，更新了更详细的游戏指引，添加遮罩（使前景对话框出现导致暂停时背景会变暗）
- 背包更新：抽奖有概率获得永久属性提升，背包物品和技能点数量加入存档/PlayerPref的继承
- 游戏性修改：修改增益机制，现在临时增益被额外保存而不是直接修改基础属性，因此不会被继承也不再乘法叠加；不安全区的伤害也会随关卡提升；将Boss粒子的伤害与Boss的ATK挂钩；

## V0.20a(2017.12.16)

- 数值修改：四个技能做了平衡，一技能的防御力提升被转移到三技能，四技能的例子攻击力与主角攻击力挂钩
- 新添了doc文件夹，可以用来刷Gi*ub

## V0.21(2017.12.23)

- 加入了手动保存的UI和操作入口
- 右上角加上了一个小UI，显示目前的关卡等级
- 金钱掉落刷到地下的Bug原因未知，怪物掉落金钱重新改为直接增加

## V0.21a(2017.12.24)

- 修改怪物模型
- 加载关卡场景改为异步加载
- 载入场景的动画优化

## V0.21b(2017.12.27)

- 游戏命名为Philosopher's Stone
- 主菜单字体统一；选人界面加入昵称输入框
- 移除状态菜单中的背包栏，替换为状态帮助；第五关开始时会弹出分享到票圈的界面
- Bug修复：Boss的粒子现在正确地只向一个方向发射，会出现明显的缺口供玩家近身战斗；修复了商店按键不灵的问题；修复了技能点数量错乱的问题；修复了地图物品不随关卡升级的问题；修复了读档后模型错乱的问题；修复了不同角色头像相同的问题；修复了三技能持续时间无限的问题。
- 创建了一个编译版本的下载链接用于展示
